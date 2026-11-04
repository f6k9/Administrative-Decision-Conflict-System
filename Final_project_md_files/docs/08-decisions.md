# ITISAQ — Confirmed Decisions

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
