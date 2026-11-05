# ITISAQ — Project Status

Last updated: 2026-11-05

## Completed

- Added the approved Report II Questions 1 and 2 to `reports/report-2.md`, recorded the related decisions in `08-decisions.md`, and updated the access-model wording in `01-project-overview.md` and `02-problem-and-scope.md`. This is documentation completion only.

- Saved the reviewed Report II Questions 3 and 4 in `reports/report-2.md` and synchronized `03-requirements.md` with the confirmed roles/accounts, uploads, reviewer assessments, saved revisions/history, data/security requirements, software/hardware baseline, and provisional model/fine-tuning plan. Preserved existing IDs, Report I source references, business rules, constraints, and evaluation obligations. Verified complete/unique requirement IDs, report wording against the reviewed source, Markdown structure, and relative links. This is documentation completion only.

- Updated the local `AGENTS.md` commit-message rule to use concise change descriptions rather than date/time and filename lists. Recorded the superseding decision in `08-decisions.md`.

- Updated `AGENTS.md` for the approved direct-to-main Pull/Push workflow, preserving local and teammate changes, reviewing conflicts, and asking for commit messages when unspecified. Recorded the decision in `08-decisions.md` and verified the documentation diff. Published to `main` and verified remote commit `bcc4a4aa892ca0df0458ce6970677d686c89f88d`. The earlier guidance-branch changes are now included in `main` as well.

- Published the latest GitHub guidance and tracking updates to `f6k9/Administrative-Decision-Conflict-System`, branch `docs/sync-project-guidance-20261104`. Verified remote commit `4f2abb54c9f1e3ec72f0c573b37680e2878dea99`. The shared `main` branch was not modified.

- Verified repository read access and prepared a task branch based on the existing `main` history, preserving the existing repository layout and other project files.

- Added the designated GitHub repository and explicit-request publishing workflow to `AGENTS.md`, and recorded the repository decision in `08-decisions.md`. No files were pushed.

- Populated `02-problem-and-scope.md` from Report I, covering the problem, target users, included work, boundaries, dependencies, and unresolved scope details. Checked consistency with the requirements and verified documentation links; no new project scope or implementation progress was asserted.

- Applied the approved startup order in `AGENTS.md`: read available core documents once per chat, including requirements, then read only task-relevant additional material. Recorded the superseding startup decision in `08-decisions.md`.

- Updated `AGENTS.md` to discover current documentation, handle missing/empty files, avoid repeated full-folder reading, and preserve approval for new topic files.
- Recorded the document-discovery policy in `08-decisions.md`.
- Created `03-requirements.md` from Project Report I: 22 functional requirements, 6 non-functional requirements/quality goals, 5 business rules, 3 constraints, and 7 evaluation/delivery requirements, each with report section references.
- Marked the extraction as an initial specification for review and separated unresolved details from report-stated requirements. Verified unique IDs, documentation links, and saved contents; this does not verify software implementation.

- Added the approved documentation organization rule to `AGENTS.md`: check existing documents first, propose a dedicated file inside `docs/` when justified, and obtain user approval before creating or splitting it.
- Recorded this documentation decision in `08-decisions.md`.

## Current work and next steps

- Report II Questions 1 to 4 are drafted in `reports/report-2.md`. Questions 5 and 6 remain to be written, and Question 6 must add fine-tuning to the schedule. Final report pagination/layout and software behavior have not been verified.
- Resolve final data schemas, exact reviewer scopes/routing, account provisioning and authentication implementation, retention/deletion policies, interface/storage/retrieval/training-tool choices, and quantitative acceptance criteria during the relevant design/evaluation work.
- Evaluate the provisional Gemma (`gemma4:12b`) model and fine-tuning feasibility on the initial local computer (Windows 11 Pro, AMD Ryzen 5 5600, 16 GB RAM, user-reported RTX 4070 SUPER). Record measured performance before defining minimum hardware or response-time guarantees. Training results have not been verified.
- The Report II Questions 3 and 4 documentation update is on `main` as commit `b589581` ("Update Report II skills and detailed requirements").
- The desktop documentation folder remains outside Git; the publishing checkout is under the project workspace at `output/itisaq-repository`, with documentation inside `Final_project_md_files/`. Preserve both copies when synchronizing. The earlier task-branch publication remains historical, not the current branch policy.
- Populate other topic documents when work reaches their stage and the user requests it. Follow the existing approval rule before introducing new topic documents.

## Blockers

- No blocker was identified for this documentation update.

This status records documentation progress only. It does not assert completion of the software prototype or reconstruct earlier project progress.
