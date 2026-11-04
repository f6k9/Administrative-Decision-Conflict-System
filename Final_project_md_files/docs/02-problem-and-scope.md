# ITISAQ — Problem and Scope

## 1. Basis and document purpose

This document summarizes the problem and proposed project boundaries in [Project Report I](../reports/report-1.md), primarily Sections 2.1–2.5, with supporting context from Sections 1.2–1.3, 3.4, 4.2, and 5.

It describes the intended prototype, not verified implementation progress or demonstrated performance. Detailed requirement IDs and unresolved specification items are maintained in [03-requirements.md](03-requirements.md). The broader project introduction is in [01-project-overview.md](01-project-overview.md).

## 2. Problem definition

Before issuing an administrative decision, organizational staff must establish whether the issuing position has authority to perform the intended action, determine the people or units affected, and review existing instructions that apply to the draft.

The relevant information may be distributed across organizational rules, existing decisions, charts, and job descriptions. Locating, reading, and comparing this information can require substantial manual work, even within an organization that manages its policies well and has no known conflicts. As the collection grows, preparation can become harder and may involve repeated corrections or delays.

ITISAQ addresses this preparation and review problem by bringing explicit organizational checks, applicable existing instructions, and potential conflict findings into a local workflow before issuance. Finding applicable instructions is valuable even when no conflict is detected.

**Source:** Report I, §§1.2, 2.1, 2.4.

## 3. Why the problem requires more than text matching

- **Authorization and content are different questions.** A draft may be consistent with existing instructions while its issuer lacks permission to perform the action.
- **Applicability matters.** Decisions must be interpreted with their actual coverage, effective dates, status, and exceptions. Similar wording does not establish that both apply to the same situation.
- **Meaning matters.** Differently worded instructions may impose incompatible requirements, while similar instructions may be compatible.
- **Shared coverage is insufficient.** Applying to the same department or activity does not by itself establish a conflict; the applicable requirements must be examined for incompatibility.
- **Hierarchy is not automatic authority.** A reporting relationship or higher rank does not grant every permission or automatically settle precedence.
- **Extraction is not confirmation.** A recovered chart relationship or job responsibility requires review and cannot independently establish administrative permission.

The project therefore combines document processing, retrieval, natural-language analysis, structured organizational information, and explicit rule-based validation.

**Source:** Report I, §§2.1, 2.4, 4.2.1–4.2.6.

## 4. Target users and operating context

The proposed prototype operates locally within a configured organization, using supplied reference decisions and reviewed organizational information.

| User group | Role within the project scope |
| --- | --- |
| Decision authors | Staff and managers preparing drafts and locating applicable instructions before issuance. |
| Administrative reviewers | Authorized personnel verifying permissions, examining potential conflicts, and determining appropriate action. |
| Configuration administrators | Personnel maintaining and confirming organizational structures, permission rules, and reference documents. |

The report specifies a simplified access model distinguishing these responsibilities. Its exact permissions and authentication mechanism remain to be defined.

**Source:** Report I, §§2.2–2.3.

## 5. In scope

| Area | Included work | Report source |
| --- | --- | --- |
| Organizational configuration | Maintain reviewed units, positions, reporting relationships, permissions, and allowed scopes in JSON. | §§1.2, 2.2 |
| Draft submission | Accept Arabic and English draft decisions with issuing position, intended action, actual coverage, and relevant dates; confirm suggested details when needed. | §§1.2, 2.4 |
| Permission and scope validation | Apply explicit Python-based organizational checks before semantic conflict analysis; explain confirmed failures and flag unclear or missing information. | §§2.2, 2.4 |
| Reference decision storage | Store supplied decisions with sources, coverage, effective dates, and status. | §2.2 |
| Applicable-instruction retrieval | Use RAG and applicability information to retrieve relevant passages, supporting Arabic and English and relevant cross-language matches. | §§2.4, 4.2.4–4.2.5, 5.3 |
| Potential conflict analysis | Use a local language model to compare eligible drafts with retrieved instructions, considering meaning and applicability. | §§1.2, 2.4 |
| Evidence and human review | Present relevant instructions, findings, explanations, supporting passages, uncertainty, and recommended administrative responses based on explicit organizational rules. | §§1.3, 2.4 |
| Draft revision | Allow users to revise and resubmit drafts before issuance. | §2.4 |
| Configuration extraction proposals | Process text or images of organizational charts, job descriptions, and official rules; match proposed information to positions, validate its structure, retain source references, and require authorized human confirmation before use. | §2.4 process A |
| Evaluation and delivery | Produce a working prototype, documented test dataset, and evaluation report; evaluate components and compare assisted preparation and review with a manual process. | §§1.2–1.3, 2.5, 4.2.7–4.2.8 |

## 6. Boundaries and exclusions

### 6.1 Human authority and final action

ITISAQ supports review before issuance. Authorized personnel remain responsible for revising and issuing decisions. System findings do not independently approve or issue a decision, and a result reporting no detected conflict is not automatic approval.

### 6.2 Explicit organizational authority

Permission, scope, and authority outcomes must follow reviewed organizational rules. The language model must not invent permissions, infer unlimited authority from rank, or treat every higher-ranking instruction as automatically taking precedence. Organizational rules must address precedence, exceptions, and delegation where applicable.

### 6.3 Supplied information and uncertainty

The prototype analyzes supplied reference decisions and configured organizational information. It cannot assume that unavailable documents or missing rules are known. Missing or ambiguous information is flagged for clarification, and uncertain findings are presented for human review. The report does not establish guaranteed detection of every conflict.

### 6.4 No automatic configuration activation

Extracted organizational information remains a proposal until its structure is checked and an authorized person confirms it. Job responsibilities do not automatically establish authority to issue decisions.

### 6.5 Prototype and technical scope

The project proposes a local prototype and a simplified access model. A full enterprise identity platform or external-system integration is not established by Report I and must not be assumed as committed scope. The initial prototype does not reproduce Self-RAG's specialized training pipeline. Specific supporting tools and final model choices remain subject to evaluation.

### 6.6 Development sequence

The core text-based review workflow will be developed first using manually reviewed organizational data. Image extraction and proposed configuration updates are planned for a later development stage; they remain within the intended project scope.

**Source:** Report I, §§1.3, 2.3–2.5, 3.4, 4.2.3–4.2.4, 4.2.6, 5.

## 7. Dependencies and working assumptions

The following dependencies follow from the proposed workflow. They identify what the project needs; they do not assert that the necessary resources have already been obtained or validated.

| Dependency | Why it matters | Report source |
| --- | --- | --- |
| Supplied reference decisions and metadata | Retrieval and applicability checks need source documents, coverage, effective dates, and status. Missing relevant material limits the analysis. | §§2.2, 2.4 |
| Reviewed organizational rules | Permission and scope checks need explicit, confirmed rules rather than assumptions about titles or hierarchy. | §§2.4–2.5, 4.2.3 |
| Authorized human reviewers | Configuration proposals need confirmation, and review findings need human assessment before final action. | §§1.3, 2.4 |
| Suitable local computer and storage | Available processor, RAM, graphics hardware, and storage constrain model operation and tool selection. Exact minimum specifications are not defined. | §5.1 |
| Project-relevant reference cases | Evaluation needs reviewed expected outcomes for authorization, retrieval, conflicts, and extraction. General benchmark results do not establish project accuracy. | §§2.5, 4.2.8, 6.2 |

Python, Ollama, and reviewed JSON configuration are specified in the report. Final language-model configuration, interface framework, storage solution, embeddings, vector store, and document-reading tools require further selection and testing.

## 8. Details still to define

Report I plans further requirements specification, data analysis, design, and tool experiments. The following are unresolved details within that process:

- Supported administrative decision categories and concrete organizational scenarios.
- Exact role permissions, allowed scopes, authority relationships, precedence, delegation, exceptions, and cancellation handling.
- Final input formats, chart layouts, schemas, decision metadata structure, and clarification interactions.
- Access permissions, interface design, and supporting storage and retrieval components.
- Final local model and hardware configuration.
- Evaluation datasets, scoring procedures, accuracy expectations, response-time limits, and criteria for meaningful efficiency improvement.

These details are tracked in the open-items section of [03-requirements.md](03-requirements.md). They must not be silently treated as finalized decisions.

**Source:** Report I, §§2.5, 4.2, 5, 6.

## 9. Intended value and evidence limits

ITISAQ aims to reduce the effort of locating applicable instructions and reviewing draft decisions while preserving human responsibility. Its evaluation must examine correctness as well as preparation/review time and perceived effort. Faster review alone does not establish better decision quality.

The report and its selected literature do not establish the reliability of the complete integrated system. Permission and scope checks, retrieval, conflict analysis, explanation quality, and configuration extraction require ITISAQ-specific evaluation. No numerical performance guarantee or completed efficiency improvement is asserted here.

**Source:** Report I, §§1.2, 4.2.7–4.2.8.

## 10. Scope changes

Any later expansion or reduction of this scope should be explicitly confirmed and recorded in [08-decisions.md](08-decisions.md). Relevant requirements should be updated when that work is requested. Preserve Report I as the historical record rather than rewriting it to match later changes.
