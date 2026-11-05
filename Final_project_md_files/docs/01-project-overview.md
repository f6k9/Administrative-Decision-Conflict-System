# ITISAQ — Project Overview

> Based on [Project Report I](../reports/report-1.md), particularly Sections 1.1–1.3, 2.1–2.5, 4.2, 5, and 6. This document explains the proposed system. Statements about preliminary work reflect the report, rather than independent verification of implementation progress.

## 1. Project identity

**Full title:** ITISAQ: Local LLM Support for Administrative Decision Review.

ITISAQ is an applied artificial intelligence and software development graduation project for CPCS498 – Project I at King Abdulaziz University, Faculty of Computing and Information Technology. The project is presented by Faris Ahmad Khayat and Sulaiman Al-Ahmadi, under the supervision of Dr. Mohammed Dahab.

The intended deliverable is a local software prototype that helps organizational staff prepare and review administrative decisions before issuance. It brings organizational authorization checks, relevant existing instructions, and potential conflict findings into one workflow for human review.

## 2. Background and problem

Preparing an administrative decision requires more than writing its text. The author must establish whether the issuing position has authority to perform the intended action, identify the people or organizational units affected, and review existing instructions that apply to the draft.

Relevant information may be spread across many documents. Locating, reading, and comparing these documents can require considerable effort, even when the organization manages its policies well and has no known conflicts. A growing collection of decisions can make preparation harder and lead to repeated corrections or delays.

Text similarity alone cannot establish a conflict. Similar instructions may apply to different departments, while differently worded instructions may impose incompatible requirements on the same situation. Review therefore needs to consider meaning, actual coverage, effective dates, exceptions, decision status, and applicable authority rules.

An authorization failure is also distinct from a content conflict: an issuer may lack permission even when the draft does not contradict an existing instruction.

## 3. Purpose and objectives

ITISAQ aims to help staff find applicable instructions and identify potential problems before issuing a decision. It aims to reduce preparation and review time and effort, with any improvement subject to evaluation.

The report defines eight objectives:

1. Represent organizational units, positions, reporting relationships, permissions, and allowed scopes in a reviewed JSON configuration.
2. Accept draft administrative decisions in Arabic and English before issuance.
3. Check the issuing position's permission for the intended action and whether the draft falls within its allowed scope.
4. Retrieve relevant existing decisions to help users understand applicable instructions.
5. Use a local large language model to identify potential conflicts between the draft and applicable existing decisions.
6. Present clear explanations and supporting passages so users can review and revise their draft.
7. Extract proposed configuration updates from organizational charts and job descriptions, match them to the correct positions, and require human confirmation before use.
8. Evaluate the system's checks and compare preparation and review time and effort with a manual process.

Finding applicable instructions remains valuable even when the system finds no conflict.

## 4. Target users

| User group | Main responsibility |
| --- | --- |
| Decision authors | Staff and managers who prepare drafts and need to locate applicable instructions before issuance. |
| Administrative reviewers | Authorized personnel who verify permissions, examine potential conflicts, and decide the appropriate action. |
| Configuration administrators | Personnel who maintain and confirm organizational structures, permission rules, and reference documents. |

The prototype is planned to use a simplified access model with three system roles: Decision Author, Administrative Reviewer, and Configuration Administrator. Each user signs in with an individual account, and one authorized user may hold several roles.

## 5. Main capabilities

### 5.1 Reviewed organizational configuration

The system will maintain organizational units, positions, reporting relationships, permissions, and allowed scopes in JSON. This reviewed configuration supplies explicit rules for authorization checks. A reporting relationship or higher organizational rank does not automatically grant every permission.

### 5.2 Permission and scope checks

Python-based rules will check whether the issuing position may perform the intended action and whether the draft stays within its permitted organizational area. Confirmed failures will be explained, while missing or ambiguous information will be flagged for clarification.

### 5.3 Relevant decision retrieval

The system will store supplied existing decisions with source information, actual coverage, effective dates, and status. Retrieval-Augmented Generation (RAG) will bring relevant passages into the review workflow. Applicability depends on these details as well as content similarity, including Arabic and English retrieval needs.

### 5.4 Local analysis of potential conflicts

After permission and scope checks pass, a locally running language model will compare the draft with retrieved instructions. It will consider whether the instructions apply to the same situation and impose requirements that cannot be followed together. Shared coverage alone does not establish a conflict.

### 5.5 Explained findings and revision

Results will include relevant instructions, authorization findings, potential conflicts, explanations, supporting passages, and uncertainty where appropriate. Explicit organizational rules will determine authority relationships and recommended administrative responses. Users can revise their draft and submit it again.

### 5.6 Proposed configuration extraction

Organizational charts, job descriptions, and official rules may be supplied as text or images. Text extraction, OCR, or a local vision-capable model will be used where appropriate. Extracted information will be matched to positions and proposed as structured configuration updates, with source references retained.

Proposals must pass structural checks and authorized human review before entering the active JSON configuration. A responsibility found in a job description must not automatically be treated as permission to issue a decision.

## 6. Main workflows

### 6.1 Preparing organizational information

1. Supply organizational charts, job descriptions, and official rules as text or images.
2. Extract the relevant text, chart relationships, and other organizational information using suitable local processing tools.
3. Propose structured information and associate extracted descriptions with the relevant positions.
4. Validate the structure and retain supporting source references.
5. Have an authorized person review and confirm the proposed information before saving it to the JSON configuration.

Development is planned to begin with manually reviewed organizational data and text-based decisions. Image extraction and proposed configuration updates will follow the core review workflow.

### 6.2 Reviewing a draft decision

1. **Receive the draft:** Collect decision text, issuing position, intended action, actual coverage, and relevant dates. Confirm suggested or extracted details when needed.
2. **Check permission and scope:** Apply explicit Python-based organizational rules. Explain confirmed failures and request clarification for missing or ambiguous information.
3. **Retrieve applicable decisions:** For drafts that pass the checks, retrieve relevant existing decisions using their status, dates, coverage, and content.
4. **Analyze potential conflicts:** Use the local model to compare the draft with retrieved instructions and examine whether their applicable requirements can be followed together.
5. **Apply organizational rules and present findings:** Show reasons, evidence, uncertainty, and recommended next steps based on explicit authority rules.
6. **Support human review and revision:** Let the user revise and resubmit the draft. Authorized personnel retain responsibility for the final decision and its issuance.

## 7. Illustrative review scenario

The following fictional example illustrates the proposed workflow; it is not a test result or an additional requirement.

An existing instruction requires a department's attendance report every Monday. A new draft requires the same department to submit that report exclusively on Wednesday instead of Monday.

ITISAQ would first check the issuing position's permission and scope. If those checks pass, it would retrieve applicable instructions and examine whether both requirements affect the same reporting activity during overlapping effective periods, taking exceptions and status into account.

If the requirements appear incompatible, the system would present a potential conflict, the supporting source passage, an explanation, and any uncertainty for review. Explicit organizational rules would guide any authority or precedence outcome. An authorized person would decide how to proceed.

If the instructions applied only to separate departments, their different reporting days would not by themselves establish a conflict. If the issuer lacked permission, that would be reported separately as an authorization failure.

## 8. Boundaries and human responsibility

- The prototype supports decision preparation and review within a configured organization before issuance.
- Organizational authorization is checked through explicit, reviewed rules; the language model does not determine permissions by assumption.
- Higher rank does not automatically grant all permissions or make an instruction take precedence. Applicable authority, precedence, exceptions, and delegation must follow configured rules.
- Analysis uses supplied decisions and organizational information. Missing information and uncertain interpretations require visible qualification or clarification.
- Findings are potential issues for human assessment. Absence of a detected conflict does not establish automatic approval.
- Extracted configuration changes require authorized human confirmation before use.
- Authorized personnel remain responsible for revising, approving, and issuing decisions.
- Local AI processing and Arabic and English support are part of the proposed scope. Specific model and supporting-tool choices require project evaluation.

## 9. Expected deliverables and evaluation

The report identifies three main deliverables:

1. A working local prototype covering organizational configuration management, draft submission, decision storage and retrieval, authorization checks, local model analysis, and evidence presentation.
2. A documented test dataset containing reviewed reference cases.
3. An evaluation report describing results and limitations.

Evaluation will examine permission and scope checks, retrieval, conflict detection, explanation quality, and configuration extraction. Manual and system-assisted preparation and review will be compared for correctness, time, and perceived effort. Retrieval and conflict-analysis errors will be assessed separately, and formal evaluation cases will remain separate from cases used to improve prompts or tune the system.

The report describes preliminary model testing and plans for further comparison, project-specific test cases, and a small prototype. It does not establish that the complete system has been implemented or that efficiency gains have been demonstrated. Detailed technical choices and ongoing progress belong in the linked documents below.

## 10. Related documentation

| Document | Detailed information |
| --- | --- |
| [README](../README.md) | Short introduction and folder navigation |
| [Project Report I](../reports/report-1.md) | Source report for this overview |
| [Problem and scope](02-problem-and-scope.md) | Detailed problem definition and project boundaries |
| [Requirements](03-requirements.md) | Functional and non-functional requirements |
| [System architecture](04-system-architecture.md) | Components, interfaces, and data flow |
| [Organizational rules](05-organizational-rules.md) | Permissions, scope, authority, and configuration rules |
| [AI and RAG](06-ai-and-rag.md) | Retrieval, local model analysis, and technical experiments |
| [Evaluation plan](07-evaluation-plan.md) | Reference cases, measures, and evaluation procedure |
| [Decisions](08-decisions.md) | Confirmed technical decisions and their reasons |
| [Project status](09-project-status.md) | Current progress and next steps |

Linked documentation files may remain empty until their content is prepared and approved.
