# ITISAQ — Requirements

## 1. Purpose and status

This document organizes the requirements extracted from [Project Report I](../reports/report-1.md). It describes the intended prototype, not completed implementation. Requirement IDs are documentation identifiers introduced here for future reference.

**Status:** Initial extraction from Report I for review and refinement. The report describes planned functionality and calls for further requirements specification; this extraction does not claim that all detailed requirements have been formally approved. Items explicitly stated in the report are separated from unresolved details. No numerical performance targets or final model selections are inferred.

Source references below identify sections of Report I. “Shall” expresses the intended requirement extracted from that source, rather than a claim that the behavior already exists.

## 2. Users and responsibilities

| User group | Responsibility stated in the report | Source |
| --- | --- | --- |
| Decision authors | Prepare draft decisions and find relevant instructions before issuance. | §2.3 |
| Administrative reviewers | Verify permissions, examine potential conflicts, and determine the appropriate action. | §2.3 |
| Configuration administrators | Maintain and confirm organizational structures, permission rules, and reference documents. | §2.3 |

The report requires a simplified access model distinguishing these responsibilities. It does not specify a complete role-permission matrix or authentication mechanism.

## 3. Functional requirements

### 3.1 Organizational configuration and access

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-01 | The system shall maintain reviewed organizational units, positions, reporting relationships, permissions, and allowed scopes in a JSON configuration. | §1.2 objective 1; §2.2 |
| FR-02 | The prototype shall distinguish decision-authoring, administrative-review, and configuration-administration responsibilities through a simplified access model. | §2.3 |
| FR-03 | Permission and authority checks shall use explicitly configured organizational rules, including precedence, exceptions, and delegation where applicable. The configured rules shall determine authority relationships and recommended administrative responses. | §2.4 step 5; §4.2.3 |

### 3.2 Draft submission and authorization checks

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-04 | The system shall accept draft administrative decisions in Arabic and English before issuance. | §1.2 objective 2; §2.2 |
| FR-05 | Draft submission shall capture decision text, issuing position, intended action, actual coverage, and relevant dates. Extracted or suggested details shall be confirmed when needed. | §2.4 step 1 |
| FR-06 | The system shall check whether the issuing position has permission to perform the intended action using explicit Python-based rules. | §1.2 objective 3; §2.4 step 2 |
| FR-07 | The system shall check whether the draft falls within the issuing position's allowed scope. | §1.2 objective 3; §2.4 step 2 |
| FR-08 | The system shall explain confirmed permission or scope failures and flag missing or ambiguous information for clarification. | §2.4 step 2 |
| FR-09 | Permission and scope checks shall precede semantic conflict comparison. Drafts that pass these checks shall proceed to applicable-decision retrieval and conflict analysis. | §2.2; §2.4 steps 2–4 |

### 3.3 Existing decisions and retrieval

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-10 | The system shall store supplied existing decisions together with their sources, actual coverage, effective dates, and status. | §2.2; §3.2 |
| FR-11 | The retrieval workflow shall index decision passages and retrieve relevant existing instructions through RAG, considering content, coverage, dates, and status to identify applicability. | §2.4 step 3; §4.2.4; §5.3 |
| FR-12 | Retrieval shall support Arabic and English inputs, including relevant decisions across languages. | §4.2.5; §5.3 |
| FR-13 | Relevant existing instructions shall be available to the user as part of decision preparation and review, including cases where no conflict is detected. | §1.2; §1.3; §2.4 |

### 3.4 Potential conflict analysis and findings

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-14 | A local language model shall compare the draft with retrieved applicable instructions to identify potential conflicts. | §1.2 objective 5; §2.4 step 4 |
| FR-15 | Conflict analysis shall consider meaning, actual coverage, effective dates, exceptions, and decision status, examining whether applicable requirements can be followed together. Text similarity or shared coverage alone shall not establish a conflict. | §2.1; §2.4; §4.2.1 |
| FR-16 | The system shall distinguish a permission or scope failure from a conflict between decision contents. | §2.1; §2.4 |
| FR-17 | Review results shall present findings, clear explanations, supporting source passages and references, recommended next steps based on organizational rules, and any uncertainty. | §1.2 objective 6; §2.2; §2.4 step 5; §4.2.2 |
| FR-18 | The interface shall allow users to review findings and supporting evidence, revise their draft, and submit it again. | §1.3; §2.4 step 6 |

### 3.5 Organizational document extraction

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-19 | The configuration-preparation workflow shall accept text or images of organizational charts, job descriptions, and official rules. | §2.4 process A |
| FR-20 | The workflow shall use text extraction, OCR, or a local vision-capable model where appropriate to extract organizational information and propose structured configuration updates. | §1.2 objective 7; §2.4 process A |
| FR-21 | Extracted descriptions and proposed organizational information shall be associated with the relevant configured positions. | §1.2 objective 7; §2.4 process A |
| FR-22 | Proposed configuration updates shall undergo structural validation, retain supporting source references, and require review and confirmation by an authorized person before being saved for use in the reviewed JSON configuration. | §2.4 process A; §4.2.6 |

## 4. Non-functional requirements and quality goals

The report establishes these qualitative needs. It does not provide complete measurable acceptance thresholds; those remain to be defined.

| ID | Requirement or quality goal | Report source | Detail still needed |
| --- | --- | --- | --- |
| NFR-01 | The prototype shall support local operation, with language-model execution through Ollama connected to the Python application. | §2.2; §5.2 | Supported deployment environment and hardware baseline. |
| NFR-02 | Arabic and English handling shall be evaluated on project-relevant cases, including administrative wording, negation, exceptions, and cross-language retrieval. | §4.2.5; §6.1–6.2 | Language-specific datasets and acceptance criteria. |
| NFR-03 | Explanations shall be clear and supported by inspectable evidence for human review. | §1.2 objective 6; §4.2.2 | Evidence-quality and explanation-quality scoring criteria. |
| NFR-04 | Permission checks, retrieval, conflict analysis, and configuration extraction shall be assessed against reviewed reference cases rather than assumed reliable from general benchmarks. | §2.5; §4.2.8 | Required accuracy levels, error tolerances, and sample sizes. |
| NFR-05 | Model and tool selection shall consider response time and the available computer's processor, RAM, graphics hardware, and storage. | §5.1–5.2; §6.1 | Target response times and resource limits. |
| NFR-06 | The project shall evaluate whether assisted preparation and review reduce time and perceived effort while preserving decision quality. Improvement is an objective to test, not an established result. | §1.2 objective 8; §4.2.7 | Comparison protocol and success thresholds. |

## 5. Business rules and project constraints

| ID | Rule or constraint | Report source |
| --- | --- | --- |
| BR-01 | Authorized personnel retain responsibility for revising and issuing decisions. System findings support human review and do not constitute autonomous issuance or approval. | §1.3; §2.4 step 6 |
| BR-02 | Higher organizational rank or a reporting relationship does not automatically grant all permissions or make every conflicting instruction take precedence. Use explicit configured authority rules. | §2.4; §4.2.3 |
| BR-03 | Decisions from peer departments shall not be treated as conflicting when each applies only to its own department. | §2.4 |
| BR-04 | Extracted job responsibilities shall not automatically establish administrative authority; an unclear responsibility shall not be treated as a confirmed permission. | §2.4 process A; §4.2.6 |
| BR-05 | Proposed organizational configuration changes shall not become active without authorized human confirmation. | §1.2 objective 7; §2.4 process A |
| CON-01 | Python is the report's specified implementation language for system logic, organizational checks, document processing, and integration; Ollama runs the local model; JSON stores reviewed organizational configuration. | §5.2–5.3 |
| CON-02 | Development shall prioritize the core text-based workflow using manually reviewed organizational information before adding image extraction and proposed configuration updates. This sequencing does not remove extraction from the planned scope. | §2.5; §3.4 |
| CON-03 | The initial prototype does not reproduce Self-RAG's specialized training pipeline. | §4.2.4 |

## 6. Evaluation and delivery requirements

These are project deliverables and evaluation obligations, rather than additional user-facing features.

| ID | Requirement | Report source |
| --- | --- | --- |
| EV-01 | Deliver a working prototype, a documented test dataset, and an evaluation report. | §1.3 |
| EV-02 | Evaluate permission and scope checks, retrieval, conflict detection, explanation quality, and organizational configuration extraction using reviewed reference cases. | §2.5; §4.2.8 |
| EV-03 | Evaluate retrieval separately from conflict analysis so retrieval failures can be distinguished from interpretation failures. | §4.2.4 |
| EV-04 | Review extracted chart relationships, textual fields, and their assignment to positions separately. | §4.2.6 |
| EV-05 | Compare manual and system-assisted preparation and review, recording correctness, time, and perceived effort. | §1.2 objective 8; §4.2.7 |
| EV-06 | Keep formal evaluation cases separate from cases used to improve prompts or adjust the system. | §3.4 |
| EV-07 | Document candidate-model comparisons using consistent datasets and conditions, including answer correctness, Arabic handling, and response time on available hardware. | §6.1 |

Section 4.2.7 proposes comparable case difficulty and controlled task order to limit learning effects. These are evaluation design proposals to refine in the evaluation plan, not completed experiments.

## 7. Open details requiring confirmation

The report identifies further specification and experiments as planned work. The following details must remain unresolved until confirmed:

| Topic | Unresolved detail | Report source |
| --- | --- | --- |
| Supported decision categories | Which categories and organizational scenarios the prototype will handle. | §2.5 |
| Organizational authority | Exact permission matrix, scopes, precedence, delegation, exceptions, and cancellation rules. | §2.5; §4.2.3 |
| Data schemas | Final JSON schema, decision record structure, and representation of coverage, dates, and status. | §2.5 |
| Missing information | Exact clarification interaction and result states when required draft or configuration details are absent or ambiguous. | §2.4; §2.5 |
| Access and interface | Specific access permissions, authentication approach, interface framework, and screen/result layouts. | §2.3; §2.5; §5.3 |
| Storage and retrieval | Database/local storage, embedding model, vector store, retrieval method, and configuration. | §3.2; §4.2.4–4.2.5; §5.3 |
| Language model | Final model and configuration. Report I shortlists Gemma (`gemma4:12b`) and Qwen (`qwen3.5:9b-q4_K_M`), with Gemma preferred in preliminary testing; neither is treated here as a final selection. | §5.2; §6.1 |
| Document processing | Extraction tools, supported input formats and layouts, and when OCR or a local vision model will be used. | §2.4 process A; §5.3 |
| Evaluation targets | Test dataset size, scoring rubrics, accuracy targets, response-time limits, and criteria for efficiency improvement. | §2.5; §4.2.7–4.2.8; §6 |

Unstated features such as an autonomous approval workflow, a complete enterprise identity system, or specific numerical performance guarantees are not established requirements in this extraction.

## 8. Maintaining this document

- Keep the IDs stable when revising existing requirements. Assign a new ID to a genuinely new requirement.
- When the user requests additions or changes, update this same file and identify whether the change comes from Report I or a later confirmed decision.
- Preserve the distinction between report-derived requirements, proposed details, and subsequently confirmed changes.
- Record later confirmed decisions in [08-decisions.md](08-decisions.md) and meaningful progress in [09-project-status.md](09-project-status.md), following `AGENTS.md`.
- Keep the original report unchanged as the historical source. Detailed architecture and evaluation procedures belong in their designated documents when those are developed.
