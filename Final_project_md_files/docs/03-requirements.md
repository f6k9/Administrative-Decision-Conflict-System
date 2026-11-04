# ITISAQ — Requirements

## 1. Purpose and status

This document maintains the project requirements originally extracted from [Project Report I](../reports/report-1.md), together with the later user-confirmed refinements documented in [Project Report II, Questions 3 and 4](../reports/report-2.md). It describes intended behavior, not completed implementation or verified results. Existing requirement IDs are preserved.

**Status:** Updated on 2026-11-04 to reflect the reviewed Report II draft. Report I section references remain attached to the original requirements; later additions and refinements are explicitly attributed to the user-confirmed Report II work. Numerical acceptance criteria and final implementation choices remain unresolved where stated.

Source columns citing section numbers refer to Report I unless a later source is explicitly identified. “Shall” defines an intended requirement, not evidence of implementation. The requirements document is the maintained specification; the report records the reviewed academic draft.

## 2. Users and responsibilities

| User group | Responsibility stated in the report | Source |
| --- | --- | --- |
| Decision authors | Prepare draft decisions and find relevant instructions before issuance. | §2.3 |
| Administrative reviewers | Verify permissions, examine potential conflicts, and determine the appropriate action. | §2.3 |
| Configuration administrators | Maintain and confirm organizational structures, permission rules, and reference documents. | §2.3 |

The later confirmed roles are **Decision Author**, **Administrative Reviewer**, and **Configuration Administrator**. One authorized user may hold multiple roles; separate employees are not required. Each user signs in with an individual account. Authors access their own drafts/history, reviewers access records within their authorized review scope, and configuration-administration access alone does not grant blanket draft access or authority to approve/issue decisions. The exact review-scope definitions, account provisioning, and authentication implementation remain open.

The Decision Author need not hold the issuing position named in the draft. Authorization checks use the identified issuing position. **Actual coverage** means the organizational units, people, or activities to which a decision applies. These refinements were confirmed during Report II preparation; see its Sections 4.1.1, 4.1.3, 4.3, and 4.5.

## 3. Functional requirements

### 3.1 Organizational configuration and access

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-01 | The system shall maintain reviewed organizational units, positions, reporting relationships, permissions, and allowed scopes in a JSON configuration. | §1.2 objective 1; §2.2 |
| FR-02 | The prototype shall distinguish decision-authoring, administrative-review, and configuration-administration responsibilities through a simplified access model, allowing one authorized user to hold multiple roles. | §2.3; later confirmed Report II §4.1.2 |
| FR-03 | Permission and authority checks shall use explicitly configured organizational rules, including precedence, exceptions, and delegation where applicable. The configured rules shall determine authority relationships and recommended administrative responses. | §2.4 step 5; §4.2.3 |

### 3.2 Draft submission and authorization checks

| ID | Requirement | Report source |
| --- | --- | --- |
| FR-04 | The system shall accept draft administrative decisions in Arabic and English before issuance. | §1.2 objective 2; §2.2 |
| FR-05 | Draft submission shall capture decision text, issuing position, intended action, actual coverage, and relevant dates. Extracted or suggested details shall be confirmed when needed. | §2.4 step 1 |
| FR-06 | The system shall check whether the issuing position has permission to perform the intended action using explicit Python-based rules. | §1.2 objective 3; §2.4 step 2 |
| FR-07 | The system shall check whether the draft falls within the issuing position's allowed scope. | §1.2 objective 3; §2.4 step 2 |
| FR-08 | The system shall explain confirmed permission or scope failures and flag missing or ambiguous information for clarification. | §2.4 step 2 |
| FR-09 | Permission and scope checks shall precede applicable-decision retrieval and semantic conflict analysis. Drafts that pass these checks shall proceed to those stages. | §2.2; §2.4 steps 2–4; later confirmed Report II §4.1.3 |

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

### 3.6 Later confirmed uploads, reviewer assessments, and saved drafts

Source: user-confirmed Report II Section 4.1.7 (2026-11-04). FR-23–FR-26 are later additions.

| ID | Requirement |
| --- | --- |
| FR-23 | The system shall allow authorized users to upload existing decisions and organizational documents through the interface. |
| FR-24 | The system shall allow draft submission through direct text entry or pasting, and through document upload. |
| FR-25 | The system shall record the Administrative Reviewer’s agreement, disagreement, or request for additional information alongside the original result and evidence. Disagreement and information requests shall include a reason. |
| FR-26 | The system shall allow authorized users to save drafts, retrieve previous reviews, and compare draft revisions while preserving the results associated with each reviewed revision. |

Supported inputs shall be as follows:

| Input category | Supported inputs |
| --- | --- |
| Draft decisions | Direct text entry or pasting, PDF, and Word (.docx). |
| Existing decisions and instructions | PDF and Word (.docx). |
| Organizational charts, job descriptions, and official rules | PDF, Word (.docx), PNG, and JPG. |

Administrative Reviewer assessments shall have the following meanings:

- Agreement: The Administrative Reviewer considers the system result supported by the available evidence.
- Disagreement: The Administrative Reviewer identifies an incorrect warning or an issue missed by the system and records a reason.
- Additional information required: The assessment remains unresolved until missing information is supplied by the Decision Author or another responsible person.

Reviewer assessments shall not automatically approve, reject, issue, or apply an administrative decision; bypass organizational permission rules; activate configuration changes; or retrain the model. Formal approval and issuance shall remain with authorized people under the organization’s process.

## 4. Non-functional requirements and quality goals

The requirements below cover operating constraints, quality goals, and evaluation obligations. Quantitative acceptance criteria shall be established before formal evaluation, informed by preliminary testing. The original Report I sources are retained; the local deployment baseline was subsequently confirmed during Report II preparation.

| ID | Requirement or quality goal | Report source | Detail still needed |
| --- | --- | --- | --- |
| NFR-01 | The initial prototype shall operate locally on a single computer, with language-model execution through Ollama connected to the Python application. Document processing, retrieval, and AI analysis shall remain local. | §2.2; §5.2; later confirmed Report II §4.2 | Minimum hardware, resource limits, and measured performance; see Section 10 for the initial environment. |
| NFR-02 | Arabic and English handling shall be evaluated on project-relevant cases, including administrative wording, negation, exceptions, and cross-language retrieval. | §4.2.5; §6.1–6.2 | Language-specific datasets and acceptance criteria. |
| NFR-03 | Explanations shall be clear and supported by inspectable evidence for human review. | §1.2 objective 6; §4.2.2 | Evidence-quality and explanation-quality scoring criteria. |
| NFR-04 | Permission checks, retrieval, conflict analysis, and configuration extraction shall be assessed against reviewed reference cases rather than assumed reliable from general benchmarks. | §2.5; §4.2.8 | Required accuracy levels, error tolerances, and sample sizes. |
| NFR-05 | Model and tool selection shall consider response time and the available computer's processor, RAM, graphics hardware, and storage. | §5.1–5.2; §6.1 | Target response times and resource limits. |
| NFR-06 | The project shall evaluate whether assisted preparation and review reduce time and perceived effort while preserving decision quality. Improvement is an objective to test, not an established result. | §1.2 objective 8; §4.2.7 | Comparison protocol and success thresholds. |

### 4.1 Later confirmed usability requirement

The following requirement was confirmed by the user on 2026-11-04 while preparing Report II Question 4; it is a later addition rather than an extraction from Report I.

| ID | Requirement | Verification approach | Detail still needed |
| --- | --- | --- | --- |
| NFR-07 | The interface shall present draft submission, system results, supporting evidence, and reviewer assessments clearly, distinguishing authorization failures, potential conflicts, and unresolved information. A no-conflict result shall be presented as no potential conflict detected in the reviewed sources, not automatic approval. | Evaluate representative tasks: submit a draft, identify its result, locate supporting evidence, record a reviewer assessment, and revise/resubmit the draft. | Task-success criteria, participant selection, and usability acceptance thresholds. |

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
| Missing information | Exact clarification routing and interface details. Agreement, disagreement, and Additional information required assessments with reasons have been confirmed. | §2.4; §2.5 |
| Access and interface | Exact reviewer scopes, account provisioning, authentication implementation, interface framework, and screen/result layouts. Individual accounts, three roles, multiple-role assignment, and high-level record access are confirmed. | §2.3; §2.5; §5.3 |
| Storage and retrieval | Database/local storage, embedding model, vector store, retrieval method, and configuration. | §3.2; §4.2.4–4.2.5; §5.3 |
| Language model | Final model and configuration. Report I shortlisted Gemma (`gemma4:12b`) and Qwen (`qwen3.5:9b-q4_K_M`). The user later selected Gemma (`gemma4:12b`) as the provisional working model for Report II; suitability and fine-tuning feasibility remain unverified. | §5.2; §6.1 |
| Document processing | Specific extraction tools, supported layouts, and OCR/vision configuration. Upload formats are confirmed in Section 3.6; begin with text inputs, then scanned PDFs/images. | §2.4 process A; §5.3 |
| Evaluation targets | Test dataset size, scoring rubrics, accuracy targets, response-time limits, and criteria for efficiency improvement. | §2.5; §4.2.7–4.2.8; §6 |

An autonomous approval/issuance workflow, a complete enterprise identity system, and specific numerical performance guarantees are not established requirements. Basic individual account sign-in and reviewer assessments are confirmed; they do not establish a full approval workflow.

## 8. Maintaining this document

- Keep the IDs stable when revising existing requirements. Assign a new ID to a genuinely new requirement.
- When the user requests additions or changes, update this same file and identify whether the change comes from Report I or a later confirmed decision.
- Preserve the distinction between report-derived requirements, proposed details, and subsequently confirmed changes.
- Record later confirmed decisions in [08-decisions.md](08-decisions.md) and meaningful progress in [09-project-status.md](09-project-status.md), following `AGENTS.md`.
- Keep the original report unchanged as the historical source. Detailed architecture and evaluation procedures belong in their designated documents when those are developed.

## 9. Data requirements — later confirmed Report II refinements

Source: user-confirmed Report II Section 4.3, saved on 2026-11-04.

ITISAQ shall store and process the information needed for organizational authorization checks, document retrieval, conflict analysis, and human review.

| ID | Data category | Required information |
| --- | --- | --- |
| DR-01 | Organizational configuration | Reviewed organizational units, positions, reporting relationships, permissions, allowed scopes, and applicable authority rules, represented in JSON. |
| DR-02 | Reference decisions and instructions | Document content, source references, actual coverage, effective dates, and status. Retrieved passages shall remain traceable to their source documents. |
| DR-03 | Draft decisions | Draft text, Decision Author identity, issuing position, intended action, actual coverage, relevant dates, and identifiable revisions. |
| DR-04 | Review records | The reviewed draft revision, authorization results, potential-conflict findings, explanations, supporting passages and references, uncertainty, and missing information. |
| DR-05 | Human assessments | Administrative Reviewer identity, agreement or disagreement with results, reasons, and requests for additional information. Assessments shall remain associated with the relevant review. |
| DR-06 | Users and access | User identities, assigned system roles, and applicable access scopes. One authorized user may hold multiple roles. |
| DR-07 | Proposed organizational updates | Extracted information, supporting sources, associated positions, and review/confirmation status. Unconfirmed proposals shall remain separate from active configuration. |
| DR-08 | Fine-tuning and evaluation datasets | Project-relevant examples and reviewed expected analyses. Training, development, and final evaluation datasets shall be kept separate. |

**Draft storage and review history**

Users shall be able to save drafts, return to previous reviews, and compare revisions. Each review shall remain linked to the draft revision it analyzed. Later revisions shall not overwrite the historical content, findings, evidence, or assessments needed to understand previous reviews.

**Access to saved records**

- Decision Authors shall access their own drafts and review history.
- Administrative Reviewers shall access records within their authorized review scope.
- Configuration-administration privileges alone shall not grant access to all drafts or review records.

**Data handling**

Arabic and English content shall be preserved for processing and evidence presentation. Organizational configuration updates shall undergo validation and authorized human confirmation before activation. Missing or ambiguous information shall remain identifiable rather than being replaced with invented values.

Final record schemas, storage technology, retention and deletion rules, and detailed review-scope definitions remain to be specified.

## 10. Software and hardware — later confirmed Report II baseline

### 10.1 Software requirements

| Component | Requirement or current selection |
| --- | --- |
| Operating environment | Windows 11 Pro, 64-bit, on the initial development and testing computer. |
| Application logic | Python shall implement organizational checks, document processing, and integration between system components. |
| Local model execution | Ollama shall run the local LLM and connect it to the Python application. |
| Local language model | Gemma (`gemma4:12b`) is the current working choice for initial development. Its suitability and fine-tuning feasibility remain subject to testing. |
| Organizational configuration | JSON shall represent reviewed organizational information and authorization rules. |
| User interface | The interface shall support draft submission, document uploads, results, evidence inspection, reviewer assessments, and saved drafts and review history. |
| Document processing | Local tools shall process Word documents and text-based PDFs. Local OCR or a vision-capable model shall support scanned PDFs and images in the later development stage. |
| Retrieval | A local embedding model and retrieval component shall support Arabic and English passages while preserving references to source documents. |
| Persistent storage | Local storage shall retain documents, draft revisions, review results, reviewer assessments, and user-related records. |
| Model fine-tuning | A local training toolchain shall support fine-tuning the pretrained model using project-relevant examples, subject to compatibility and hardware feasibility testing. Fine-tuning tools shall be separate from Ollama’s model-execution role. |

### 10.2 Hardware requirements

The initial prototype shall run locally on the following development and testing computer:

| Component | Available specification |
| --- | --- |
| Operating system | Windows 11 Pro, 64-bit |
| Processor | AMD Ryzen 5 5600 |
| Installed RAM | 16 GB |
| Graphics card | NVIDIA GeForce RTX 4070 SUPER |
| Storage | Sufficient local storage for application dependencies, model files, uploaded documents, retrieval indexes, saved records, and training data. Required capacity shall be determined through testing. |
| Deployment | One computer running all prototype components locally. |

This configuration is the available development and testing environment, not a verified minimum specification.

Inference, document processing, retrieval, and fine-tuning shall be assessed separately because their resource requirements differ. Minimum hardware requirements and any necessary adjustments shall be determined through testing of the selected models, tools, and datasets.

Source: user-confirmed Report II Section 4.4 (2026-11-04). Fine-tuning is planned experimentation subject to feasibility; it does not establish specialized Self-RAG training or a demonstrated improvement. Initial testing may load documents manually; this does not replace planned interface uploads.

## 11. Security requirements — later confirmed Report II refinements

ITISAQ shall protect organizational information and restrict system operations according to authenticated user identities, assigned roles, and authorized scopes. System access permissions shall remain distinct from organizational authority to issue administrative decisions.

| ID | Requirement |
| --- | --- |
| SEC-01 | Each user shall authenticate through an individual account before accessing protected system functions and records. |
| SEC-02 | The system shall enforce access permissions for Decision Authors, Administrative Reviewers, and Configuration Administrators. An authorized user may hold multiple roles. |
| SEC-03 | Decision Authors shall access their own drafts and review history. Administrative Reviewers shall access records within their authorized review scope. Configuration-administration privileges alone shall not grant access to all drafts or review records. |
| SEC-04 | Organizational documents, drafts, retrieval data, and AI processing shall remain within the local environment. Project information shall not be transmitted to external services without explicit authorization. |
| SEC-05 | Organizational configuration changes shall require validation and confirmation by an authorized person before activation. Extracted document content shall not automatically modify active permissions or authority rules. |
| SEC-06 | Reviewer assessments shall be associated with the authenticated Administrative Reviewer and the relevant review record. Recording an assessment shall not bypass organizational authorization checks or alter the original system findings. |

Source: user-confirmed Report II Section 4.5 (2026-11-04). SEC-01–SEC-06 express intended behavior, not verified security testing.

## 12. Report II constraint identifiers

| ID | Requirement or constraint |
| --- | --- |
| AR-01 | ITISAQ shall support human review before decision issuance. It shall not autonomously approve, issue, or apply administrative decisions. |
| AR-02 | Organizational authorization checks shall remain separate from LLM-based conflict analysis. The model shall not invent authority or assume that higher organizational rank automatically grants permission. |
| AR-03 | System results shall be limited to the available organizational configuration and reference sources. Missing evidence and uncertain interpretations shall be identified explicitly. |

Source: Report II Section 4.6. AR-01–AR-03 restate existing human-review, authority-separation, and evidence boundaries; they do not replace BR-01–BR-05, CON-01–CON-03, or EV-01–EV-07. Omitting development/evaluation rows from the academic report does not revoke those existing requirements.
