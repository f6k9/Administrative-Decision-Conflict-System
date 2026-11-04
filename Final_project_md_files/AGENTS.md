# ITISAQ — Agent Instructions

## Project purpose

ITISAQ is a graduation project for supporting the review of draft administrative decisions before issuance. It checks organizational permissions and scope, retrieves relevant existing decisions, and identifies potential conflicts with explanations and supporting evidence.

The system supports human reviewers. It does not issue or approve decisions.

## Before starting work

At the beginning of each new chat in this project, check which core files exist and read the following non-empty files in this order before starting the task:

1. `README.md`
2. `docs/01-project-overview.md`
3. `docs/02-problem-and-scope.md`
4. `docs/03-requirements.md`
5. `docs/08-decisions.md`, then `docs/09-project-status.md`
6. After this core reading, locate and read only the additional documents and sections needed for the user's current task. Use current file names and targeted heading searches to find them; do not read every Markdown file merely to build an inventory.

- Perform the core reading once at the start of the chat, not before every message. Reuse context already read, and reread a file when it has changed, a detail needs checking, or verification requires it.
- Skip files that are missing or empty. Treat them as unavailable context; do not invent their contents, assume approval, or recreate them merely because a link or instruction mentions them.
- If missing information materially affects the task, ask for clarification; otherwise continue with the available sources.
- Read additional material when task dependencies, uncertainty, or conflicting information require it.

Documentation is developed incrementally. A future document name is a proposed location, not a requirement that the file already exist.

## Sources of truth

- Follow the user's explicit instructions for the current task.
- Use approved requirements and confirmed design decisions as the project reference.
- Treat proposed ideas and undecided technologies as unconfirmed.
- Treat academic reports as historical records of what was submitted.
- If documents conflict and the answer affects the task, explain the conflict and ask for clarification.

## Project boundaries

- Do not invent requirements or expand the approved scope.
- Preserve the separation between organizational authorization checks and AI-based conflict analysis.
- Use explicit, reviewed organizational rules for permission and scope checks. Do not let the LLM invent authority.
- Do not assume a reporting relationship or higher position automatically grants permission.
- Keep AI processing local as specified by the approved project scope.
- Support Arabic and English as defined in the requirements.
- Present potential conflicts with supporting source passages.
- Make uncertainty and missing information visible.
- Require authorized human review before applying extracted organizational configuration updates.

## Working rules

- Inspect existing files before making changes.
- Make focused changes that address the requested task.
- Follow the project's established structure and conventions.
- Do not overwrite unrelated work.
- Do not modify academic reports unless explicitly requested.
- Do not add external services, paid dependencies, or send project data outside the local environment without explicit approval.
- Never include passwords, API keys, or private organizational data in code or documentation.
- Ask for clarification when a missing requirement would materially change the implementation.

## GitHub repository and publishing

- Project repository designated by the user: https://github.com/f6k9/Administrative-Decision-Conflict-System
- Repository identity: `f6k9/Administrative-Decision-Conflict-System`. This URL identifies the intended repository; it does not establish that the current folder is a Git checkout, that a remote is configured, or that authentication and write access are available.
- When the user explicitly asks to upload or push the project changes (for example, "ارفعه"), treat that as authorization to review, commit, and push the relevant changes to this repository. Do not push merely because files were edited or tracking documents were updated.
- Before publishing, verify the actual working directory, Git root, remote URL, current branch, worktree changes, and relevant remote state. Do not publish to an unrelated repository or silently replace an existing remote.
- If the folder is not connected to the repository, inspect repository access and existing contents before setting up a suitable checkout within the user's authorized scope. Preserve local documents and remote history; do not blindly initialize and push over an existing project. Explain any required sign-in or missing write access without requesting passwords or tokens in chat.
- Review the diff and run appropriate checks. Include only files relevant to the requested upload, including associated decision/status updates when applicable. Preserve unrelated work and exclude credentials, private local configuration, and temporary artifacts.
- For concurrent team work, use an appropriate task branch. Do not directly push to the shared default branch or merge a pull request unless the user explicitly requests or has already authorized that workflow. If an upload request concerns a clearly established task branch, continue on that branch; if the intended destination remains ambiguous, ask which branch to use.
- Never force-push, discard a teammate's changes, or overwrite remote history to resolve divergence. Inspect and combine compatible changes. For files 08 and 09, retain compatible confirmed decisions and verified progress from both contributors; ask about contradictory decisions or uncertain claims rather than choosing a version arbitrarily.
- After publishing, report the repository, branch, commit identifier, and what was uploaded. Verify push success before claiming publication. If blocked, distinguish local saved changes or commits from changes actually pushed.

## Documentation

- Keep each topic in its designated document and link to it from other files.
- Populate other documentation files when the user requests work on their topic or stage. Do not automatically fill or update them as part of routine documentation tracking.
- Automatic documentation tracking is limited to `docs/08-decisions.md` and `docs/09-project-status.md`, as described below.
- Clearly distinguish completed work, planned work, proposals, and unresolved questions.

### Handling added, deleted, or renamed documents

- Discover topic documents from the current folder contents rather than maintaining an exhaustive file list in `AGENTS.md`. Adding or removing an ordinary topic document does not require changing this instruction file.
- Check that a referenced file exists before opening it. Old links and navigation lists may be outdated and must not override the actual inventory.
- When the user authorizes adding, deleting, or renaming a document, include necessary navigation/link repairs in that change. Update `AGENTS.md` only if a workflow rule or a specifically referenced core path actually changes.
- Do not delete, rename, or recreate documents merely to make the folder match an earlier scaffold. Propose new topic files in the chat and follow the approval rule below.
- Continue automatic tracking for files 08 and 09 under the existing rules. This does not authorize creating other missing topic documents.

### Organizing topic-specific documentation

- After the required startup reading, read the documents and sections relevant to the current task. Do not repeatedly read every Markdown file without a task-related reason. Read additional material when dependencies, uncertainty, or conflicting information require it.
- Before proposing a new document, check existing document names, headings, and relevant contents to see whether an appropriate file already covers the topic.
- If the current topic has no suitable document, or has become substantial enough to benefit from a separate document, suggest a dedicated Markdown file inside `docs/` in the chat. Explain why it would help and propose a clear filename and scope.
- Wait for the user's approval before creating the proposed file or splitting or moving existing documentation. A suggestion is not approval.
- Prefer the existing topic document for small additions. Do not create a separate file for every diagram or minor discussion.
- For example, use an existing architecture document for architecture diagrams. If none exists, propose a suitable file such as `docs/04-system-architecture.md` and obtain approval before creating it. If diagram documentation later becomes substantial, propose a separate file such as `docs/system-diagrams.md` before splitting it.
- After an approved split, keep one authoritative location for each topic and use links from related documents instead of duplicating information. Update navigation as needed within the approved scope.
- Organization helps reduce irrelevant reading and conflicting information; it does not guarantee correctness. Ground content in available sources and confirmed decisions, and flag missing information rather than inventing it.

### Automatic decision tracking: docs/08-decisions.md

- Update this file without asking for permission each time the user explicitly confirms a project decision or a decision is clearly established by approved work.
- Record the confirmed decision, its reason when known, and relevant context. Do not invent a reason that was not established.
- Do not treat suggestions, experiments, candidate technologies, or unanswered questions as final decisions.
- Read existing entries before updating. Avoid duplicates and preserve decision history; clearly identify a later decision that supersedes an earlier one.

### Automatic progress tracking: docs/09-project-status.md

- Update this file without asking for permission after meaningful, verified project progress or a confirmed change to current work, next steps, or blockers.
- Keep a concise view of completed work, current work, next steps, and blockers when applicable.
- Mark work as completed only when it has actually been completed. Distinguish planned features and report statements from implementation verified in the workspace.
- Read the existing status first, retain relevant information, and remove or revise outdated status when justified by the work.

### Scope and chat notification

- Initialize file 08 or 09 if it is empty when a relevant tracking event occurs. Do not backfill unrelated history or update either file merely because a chat occurred.
- These automatic updates do not authorize edits to other documentation files or academic reports.
- Whenever either file is actually updated, explicitly tell the user in the final chat response which file was updated and briefly what changed, using the user's conversation language.
- Mention only files that were actually updated. Do not claim a successful update if saving or verification failed; explain the issue instead.
- Example when both files were updated: "حدّثت `08-decisions.md` لتسجيل القرار المتفق عليه، وحدّثت `09-project-status.md` لإضافة العمل المنجز والخطوة التالية."

## Verification and reporting

- Run checks appropriate to the change.
- Never claim that tests passed unless they were run successfully.
- Do not invent evaluation results, references, or implementation progress.
- After completing work, summarize what changed, what was verified, and any remaining issues.
