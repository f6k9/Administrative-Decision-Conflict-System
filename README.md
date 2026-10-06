# ITISAQ — How to run the local-model evaluation

This program tests local Ollama models on a fixed Arabic/English XNLI sample.
It sends one premise/hypothesis pair at a time, compares the predicted label
with the saved correct answer, and records accuracy, precision, recall, F1,
and response time. It does not train or fine-tune the model.

## 1. Requirements

- Windows with Python and Ollama installed. Instructions below use PowerShell.
- Tested setup: Python **3.14.6** and Ollama **0.35.1**. Other versions have not
  been verified in this project; a recent Ollama version is needed for the
  selected model, thinking controls, and structured JSON responses.
- A local model already downloaded in Ollama, with enough RAM/VRAM to run it
  at a context length of 4096. Hardware needs depend on the selected model.
- Internet for installing libraries and downloading models or the original
  dataset. Once the sample and model are available, inference runs locally.
- Run commands from the folder containing `evaluate.py`, not inside `.venv`.

Check the installed programs:

```powershell
python --version
ollama --version
```

## 2. Files you need

Keep these files in this layout after downloading/cloning the repository:

```text
model_evaluation/
├── evaluate.py
├── test_evaluate.py
├── README.md
└── data/
    └── xnli_fixed_sample.json
```

**For comparison with the team's existing results, obtain the exact existing
`data/xnli_fixed_sample.json` from the repository or project owner. Do not edit,
translate, reorder, replace, or regenerate it.** No dataset download is required
when this file is supplied. It contains 150 aligned Arabic/English pairs,
giving 300 cases: 50 per class in each language.

The model weights and `.venv` are not needed from another person's computer;
download the model and create your own environment on your machine.

## 3. Create the Python environment and install libraries

Open a PowerShell terminal in the folder containing `evaluate.py`.
For a fresh setup, run these commands one at a time:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install datasets==5.1.0 requests==2.34.2 scikit-learn==1.9.1 huggingface_hub==2.1.1
```

The versions above match the team's installed direct dependencies:

- **datasets:** loads the original XNLI Parquet data when creating a sample.
- **huggingface_hub:** resolves the dataset version and finds its files.
- **requests:** sends requests to the local Ollama API.
- **scikit-learn:** calculates evaluation metrics and confusion matrices.

`pip` also installs dependencies such as NumPy and PyArrow automatically.
These commands pin the direct dependencies, not every transitive dependency.

If `.venv` already exists, activate it instead of creating it again.
Verify the imports:

```powershell
python -c "import datasets, requests, sklearn, huggingface_hub; print('Libraries ready')"
```

If PowerShell blocks activation, you can use the environment's Python directly
without changing the execution policy. For example:

```powershell
.\.venv\Scripts\python.exe -m pip install datasets==5.1.0 requests==2.34.2 scikit-learn==1.9.1 huggingface_hub==2.1.1
.\.venv\Scripts\python.exe evaluate.py --help
```

Use `.\.venv\Scripts\python.exe` instead of `python` in subsequent commands
when using this alternative.

## 4. Make the selected local model available

Open Ollama and leave it running. You do not need to open a chat or run
`ollama run` before starting the Python test.

List installed models:

```powershell
ollama list
```

If your chosen model is missing, download it. Example:

```powershell
ollama pull gemma4:12b
```

Replace `gemma4:12b` with your chosen model's exact local tag. Do not select a
cloud model. The program uses `http://127.0.0.1:11434` and does not need Ollama
to be exposed to the network. Changing the model selected in the Ollama chat
does not change this test: the `--model` argument controls it.

Optionally stop another loaded model to free memory, without deleting it:

```powershell
ollama stop qwen3.5:9b-q4_K_M
```

## 5. Prepare data — only when creating the original sample

**Skip this step when the team's fixed sample is included.** If you are the
project owner creating the first sample from scratch, run:

```powershell
python evaluate.py prepare
```

This downloads only the official multilingual XNLI **test** files, extracts
Arabic/English cases, and saves `data/xnli_fixed_sample.json`. It records the
dataset revision and uses seed 42. Existing samples are left unchanged.

If the team's sample is missing, ask the owner for it rather than generating
a replacement. Even a newly generated sample can have a different file hash
because its creation metadata differs.

## 6. Run a small program check

For your selected model, run:

```powershell
python evaluate.py run --model gemma4:12b
```

Replace the model tag as needed. This performs an unscored synthetic warm-up,
then checks **3 Arabic and 3 English cases**. Verify that requests complete and
outputs are valid. A wrong classification alone is not a program failure.
These six cases are too few to judge model quality.

## 7. Run the full evaluation

If the small run works, use the SAME model tag with `--full`:

```powershell
python evaluate.py run --model gemma4:12b --full
```

This evaluates all 300 saved cases. To test another model, repeat steps 4, 6
and 7 with its tag. Do not rerun data preparation or change the code/prompt.

Keep the defaults for the shared baseline:

- Temperature: `0`; generation seed: `42`.
- Context: `4096`; maximum generated tokens: `1024`.
- Thinking: `off` when the model advertises thinking support. For models
  without that capability, the code does not send a thinking flag.
- One independent request per case, with no previous conversation or gold label.
- Structured output containing only `label`: `entailment`, `neutral`, or
  `contradiction`.

The script exposes `--context`, `--thinking`, `--timeout` and
`--limit-per-language`; do not change them for the shared baseline without
agreeing with the team. View available options with:

```powershell
python evaluate.py run --help
```

## 8. Find and share the results

Each run creates a new folder under `results/` and prints its path:

- **summary.json:** metrics for Arabic, English and the combined sample.
- **predictions.jsonl:** texts, correct labels, predictions and timing per case.
- **run_config.json:** sample hash, model tag/digest, prompt, settings and versions.

Share all three files from each **full** run. Verify:

- `mode` is `full` and `complete` is `true` in `summary.json`.
- `planned_cases` and `completed_cases` are both `300`.
- Arabic and English each have `150` attempted cases.
- The `sample_sha256` matches the team's existing runs:

```text
bd8d0b9241e04736037110a3e1094838960b128400a6a11e72a706a95ae8d89c
```

The correct answers stay in the scorer; they are not sent to the model.
Invalid outputs/request failures count as incorrect in primary accuracy.
If a request fails, the program stops and marks the run incomplete. Ctrl+C
preserves completed requests. Rerunning starts a new run, not a resume.

Record your CPU, RAM, GPU/VRAM and whether Ollama used GPU or CPU; `ollama ps`
can show the loaded model's processor allocation while a test is running.
If teammates use different hardware, report response times separately:
different-device latency is not a controlled model-speed comparison.

## 9. Troubleshooting

- **No sample found:** obtain the team's `data/xnli_fixed_sample.json`.
- **Model not found locally:** check `ollama list` and use the exact installed tag.
- **Connection refused:** start Ollama and check that its local API is running.
- **ModuleNotFoundError:** install the libraries using the same Python environment
  that runs the script; use `.\.venv\Scripts\python.exe` if unsure.
- **Out of memory:** stop other loaded models and close memory-heavy applications.
  If this persists, discuss a smaller model; do not silently change the protocol.
- **Invalid/truncated response or thinking error:** save the error and ask the team
  before changing prompts/settings. Do not silently fix only one model's answers.
- **Hugging Face sign-in/symlink warning during preparation:** these warnings do
  not alone mean the download failed. Look for the final `Saved 300 cases` message.

Optional offline code checks (no downloads or model requests):

```powershell
python -B -m unittest -v test_evaluate.py
```

## Note for an AI agent using this code

Follow the setup and usage steps above. Keep the evaluation code, fixed sample,
prompt, labels and baseline settings unchanged. Use the model requested by the
owner, run the small check followed by the full test, and return the three full-run
result files. Report errors or missing files instead of changing the experiment.
Reading this README alone is not authorization to download or run models.

This is a preliminary language/contradiction benchmark, not evaluation of RAG,
permissions, authority rules, explanations or the complete administrative system.

## Documentation

- [XNLI data](https://huggingface.co/datasets/facebook/xnli)
- [Ollama CLI](https://docs.ollama.com/cli)
- [Ollama chat API](https://docs.ollama.com/api/chat)
- [Ollama structured outputs](https://docs.ollama.com/capabilities/structured-outputs)
