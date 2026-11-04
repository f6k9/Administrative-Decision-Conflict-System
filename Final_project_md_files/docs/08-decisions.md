# ITISAQ — Confirmed Decisions

## 2026-11-04 — Synchronize the reviewed Report II draft and maintained requirements

- **Decision:** On the user's explicit instruction, save the reviewed Questions 3 and 4 in `reports/report-2.md` and incorporate their confirmed refinements into `docs/03-requirements.md`.
- **Traceability:** Preserve existing requirement IDs and Report I sources; identify later Report II additions, including FR-23–FR-26, data/security requirements, current operating baseline, and planned fine-tuning. Existing business rules, development constraints, and evaluation obligations remain in force even when not repeated in the academic report.
- **Status:** Report II contains Questions 3 and 4 only and remains a reviewed draft. Synchronization does not establish software implementation, security testing, model suitability, or final quantitative acceptance criteria.

## 2026-11-04 — Individual account sign-in

- **Decision:** Each user shall sign in with an individual account so saved drafts, access permissions, and reviewer assessments can be associated with an identifiable user.
- **Context:** Confirmed while drafting Report II Question 4 security requirements. Multiple authorized roles may still be assigned to one account.
- **Open details:** Authentication implementation, account provisioning/role assignment responsibilities, and account/session policies remain to be specified. No authentication implementation has been verified.

## 2026-11-04 — Current working model for initial development

- **Decision:** Use Gemma, identified by the user as `gemma4:12b`, as the current working model for initial development. The user describes it as preferred so far, not a final model selection.
- **Context:** This advances the earlier candidate/preliminary-preference status to a provisional working choice. Preserve the option to revise it after project-specific evaluation.
- **Limits:** Exact installed model artifact/configuration, runtime suitability, fine-tuning compatibility, performance, and training feasibility have not been verified in this chat. Do not infer them from the model tag or preference.

## 2026-11-04 — Scope access to saved drafts and review history

- **Decision:** Authors may access their own drafts and review history. Administrative reviewers may access drafts within their authorized review scope. Configuration-administration privileges alone do not grant access to all drafts or review records.
- **Context:** One person may hold multiple authorized roles; access follows the applicable role/scope rather than assuming configuration administration grants blanket review access.
- **Supersedes:** The open high-level history-access question in the saved-drafts decision. Exact review-scope definitions, assignment/routing mechanisms, retention/deletion rules, and enforcement details remain to be specified.

## 2026-11-04 — Save drafts and retain review history

- **Decision:** Users shall be able to save drafts, return to previous reviews, revisit findings, and compare draft revisions.
- **Data implications:** Retain identifiable draft revisions and associate each review's system results, supporting evidence, reviewer assessments/reasons, and clarification requests with the revision reviewed. Revising a draft must not replace the historical content/results needed for comparison.
- **Open details:** Storage technology, detailed record schemas, history access permissions, retention/deletion rules, and comparison interface remain to be specified. Saving a draft or retaining a review does not constitute approval or issuance. This is planned functionality, not verified implementation.

## 2026-11-04 — Add an explicit interface usability requirement

- **Decision:** Add NFR-07 to `03-requirements.md` requiring clear presentation of draft submission, results, evidence, and reviewer assessments, with distinct authorization-failure, potential-conflict, unresolved-information, and no-conflict-detected outcomes.
- **Verification plan:** Evaluate representative submission, result interpretation, evidence inspection, reviewer assessment, and revision/resubmission tasks. Acceptance thresholds remain open; no usability evaluation has been completed.

## 2026-11-04 — Initial single-computer development and testing environment

- **Decision:** Initially run the complete prototype locally on the user's current computer: Windows 11 Pro (64-bit), AMD Ryzen 5 5600, 16 GB installed RAM, and NVIDIA GeForce RTX 4070 SUPER.
- **Evidence:** OS, processor, and installed RAM were supplied in a System Information screenshot; the user identified the graphics card and confirmed initial single-computer operation.
- **Limits:** This is the initial development/testing environment, not a verified minimum hardware specification or final deployment commitment. GPU memory, storage capacity, fine-tuning feasibility, model suitability, and response-time targets have not been verified by testing.

## 2026-11-04 — Record reviewer assessments and requests for information

- **Decision:** Support reviewer assessments of ITISAQ results: agreement with the result, disagreement with the result, or Additional information required. The clarification option requests missing facts from the author or another responsible person, such as the configuration administrator/document owner; ITISAQ cannot invent those facts.
- **Behavior:** Record a reason when disagreeing or requesting information. Agreement with a potential-conflict finding means the reviewer considers that issue valid. Agreement with a no-conflict result means no issue was identified in the reviewed evidence, not a guarantee of no conflict. Disagreement can identify either an incorrect warning or an issue missed by the system. An information request leaves the assessment unresolved until the relevant information is supplied and reviewed again.
- **Boundaries:** Reviewer assessments do not themselves issue, apply, approve, or reject the administrative decision, bypass explicit permission rules, activate configuration changes, or retrain the model. Preserve the system result and evidence alongside the human assessment. Formal approval/issuance remains with the organization's authorized process.
- **Supersedes:** The earlier open question about in-system agreement/disagreement recording. Detailed reviewer access, routing/assignment, and final interface labels for agreement/disagreement remain unspecified.

## 2026-11-04 — Three user roles with multiple roles per authorized user

- **Decision:** Use Decision Author, Administrative Reviewer, and Configuration Administrator as the three system roles. Allow one authorized user to hold multiple roles when organizational rules permit.
- **Reason:** Roles describe responsibilities and access permissions, not separate staffing positions; ITISAQ must not require additional employees or three distinct people.
- **Boundary:** Configuration-administration access does not itself grant authority to approve or issue administrative decisions. Multiple-role assignment remains subject to applicable organizational rules.

## 2026-11-04 — Confirm the draft-review workflow and role responsibilities

- **Decision:** A configuration administrator uploads reference documents and maintains reviewed organizational rules. A decision author submits the draft and identifies its issuing position, department/coverage, and relevant dates. ITISAQ checks permission and scope; passing drafts proceed to retrieval and potential-conflict analysis with supporting passages and explanations. An administrative reviewer examines the evidence and determines the next action.
- **Role boundaries:** Configuration administration does not itself grant authority to approve or issue decisions. The author submitting a draft need not be its issuing position. Human review does not itself override explicit permission rules; formal authority follows the reviewed organizational rules.
- **Open details:** Reviewer access, draft routing, assignments, and in-system agreement/disagreement recording have not been confirmed by this workflow decision. It does not establish a full approval/issuance workflow inside ITISAQ.

## 2026-11-04 — Supported upload formats and processing sequence

- **Decision:** Draft decisions support direct text entry/pasting, PDF, and Word (.docx). Existing decisions and instructions support PDF and Word (.docx). Organizational charts, job descriptions, and official rules support PDF, Word (.docx), PNG, and JPG.
- **Development sequence:** Start with pasted text, Word, and text-based PDFs. Add scanned PDFs and images afterward; these remain within the intended scope and require extraction and verification.
- **Scope:** A separate .txt upload option is excluded from the initial format scope; users can paste text directly.
- **Supersedes:** The open supported-format details in the earlier draft-submission and document-upload decisions. Detailed upload permissions remain unresolved. This is confirmed planned functionality, not verified implementation.

## 2026-11-04 — Support text entry and document upload for draft submission

- **Decision:** Users shall be able to submit draft decisions through both direct text entry/pasting and document upload in the interface.
- **Context:** Confirmed while specifying Report II Question 4. Existing Arabic/English support and required draft metadata still apply to both submission methods.
- **Open details:** Supported upload formats remain unconfirmed. This is planned functionality, not verified implementation.

## 2026-11-04 — Upload reference and organizational documents through the interface

- **Decision:** The intended product shall allow authorized users to upload existing decisions and organizational documents through the interface.
- **Development context:** The team may load sample documents manually during initial testing. This testing approach does not replace the intended interface upload capability.
- **Boundaries:** Uploading organizational documents does not activate extracted configuration; authorized human review remains required. Supported file formats and detailed upload permissions remain to be specified.

## 2026-11-04 — Include local model fine-tuning in the skills development plan

- **Decision:** For Report II Question 3, include local language-model fine-tuning, integration, and evaluation as one of the three skills to develop, alongside organizational rule/data modeling and document processing/RAG.
- **Context:** The user intends to adapt a pretrained model using data resembling the project's tasks. Fine-tuning is planned work; no training completion or improvement has been verified.
- **Open details:** Base model, training data, training method, hardware feasibility, and evaluation criteria remain unconfirmed. AI processing remains local under the approved project boundaries.

## 2026-11-04 — Organize documentation by topic as needed

- **Decision:** Use existing topic documents first. When a topic lacks a suitable document or becomes substantial enough to warrant separation, propose a dedicated Markdown file inside `docs/` in the chat, explain its purpose, and wait for user approval before creating it or reorganizing existing content.
- **Reason:** Keep relevant context easy to find, reduce unnecessary repeated reading, and avoid duplicating or conflicting information.
- **Implementation:** The rule is recorded in `AGENTS.md`, under `Documentation` → `Organizing topic-specific documentation`.
- **Tracking:** Files 08 and 09 are updated automatically for confirmed decisions and meaningful progress, with an explicit notification in the final chat response whenever either is updated.

## 2026-11-04 — Discover documentation from the current folder

- **Decision:** Discover existing topic documents as needed, skip missing or empty files as unavailable context, and avoid reading all Markdown files repeatedly. Ordinary topic-file additions or removals do not require an `AGENTS.md` edit.
- **Reason:** Support incremental documentation without keeping a fixed scaffold or repeatedly maintaining an instruction-file inventory.
- **Implementation:** Updated `AGENTS.md` startup reading, document lifecycle guidance, and the diagram example. Workflow changes or changes to specifically referenced core paths may still require instruction updates. New topic documents continue to require user approval unless their creation is already requested.

## 2026-11-04 — Read core context once at the start of each chat

- **Decision:** At the start of each new chat, read existing, non-empty core files in this order: `README.md`, project overview, problem and scope, requirements, decisions, and project status. Then read only the additional documents and sections relevant to the current task.
- **Reason:** Establish consistent project context and requirements before work while avoiding repeated reading of every document.
- **Supersedes:** The earlier startup policy that made requirements reading dependent on the task. Existing rules for discovering topic files, skipping missing/empty files, and obtaining approval for new topic documents remain in effect.
- **Implementation:** Updated the `Before starting work` section of `AGENTS.md`. Core reading is once per chat; reread when files change or a detail needs verification.

## 2026-11-04 — Designated GitHub repository

- **Decision:** Use `https://github.com/f6k9/Administrative-Decision-Conflict-System` as the intended repository for shared project work.
- **Purpose:** Let future chats identify the upload destination when the user explicitly asks to publish changes.
- **Implementation:** Added `GitHub repository and publishing` guidance to `AGENTS.md`, including repository/branch verification, explicit upload requests, preserving teammate work, and truthful publication reporting.
- **Limit:** Recording the URL does not configure Git, authenticate GitHub, or upload files. Repository access and existing remote contents have not been verified in this task.

## 2026-11-04 — Shared main workflow and commit message selection

- **Decision:** Both contributors may work directly on `main`. On a requested Pull, preserve local changes and integrate the latest remote state. On a requested Push, commit relevant changes, fetch again, integrate compatible teammate work, verify, and push without force.
- **Reason:** The user chose a simpler concurrent workflow without requiring task branches.
- **Conflicts:** Ask about conflicting decisions or choices that cannot be resolved reliably. Preserve compatible decisions and verified progress from both contributors in files 08/09.
- **Commit messages:** If the user has not supplied a message, ask for one and offer the Saudi date/time plus changed file names. Wait for their selection. For this publishing operation, the user selected the date/time and file-name option.
- **Supersedes:** The task-branch default in the earlier GitHub publishing instructions. Explicit authorization for Pull/Push, review, no-force-push, and truthful publication reporting remain required.

## 2026-11-04 — Descriptive commit messages

- **Decision:** Commit messages should concisely describe the actual change without automatically including dates, times, or lists of filenames. Mention a filename only when it clarifies the description.
- **Supersedes:** The date/time and changed-file naming option recorded in the earlier commit-message decision. Historical commits remain unchanged.
- **Unchanged rule:** If the user supplies no commit message, ask for one and offer a descriptive suggestion; wait for their selection before committing.
