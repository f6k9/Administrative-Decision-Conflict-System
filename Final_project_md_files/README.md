# ITISAQ

## General idea

ITISAQ is a graduation project for a local AI-powered administrative decision-support system. It is designed to help organizations prepare and review draft administrative decisions before they are officially issued.

The proposed system checks whether the issuing position has the required permission and organizational scope, retrieves relevant existing decisions and instructions, and analyzes potential conflicts. It presents explanations and supporting source passages so a human reviewer can assess the findings.

ITISAQ supports human reviewers. Responsibility for approving and issuing decisions remains with authorized people.

## The problem

Organizations accumulate many administrative decisions, regulations, and internal instructions. Reviewing a new draft manually can be time-consuming, and reviewers may overlook an applicable instruction, a conflict, or a limitation on the issuer's authority.

ITISAQ aims to make relevant information easier to find and help reviewers identify potential problems before a decision is issued.

## Planned main features

- **Permission and scope checking:** Validate the issuing position's authority using explicit, reviewed organizational rules.
- **Relevant document retrieval:** Use Retrieval-Augmented Generation (RAG) to find potentially applicable existing decisions and instructions.
- **Potential conflict analysis:** Use a locally running language model to compare the draft with retrieved instructions, considering meaning, scope, dates, exceptions, and decision status.
- **Evidence-supported findings:** Present explanations and original source passages for human review, including uncertainty or missing information.
- **Organizational information extraction:** Propose structured information from organizational charts and job descriptions, subject to authorized human review before configuration updates are applied.
- **Arabic and English support:** Support administrative text and retrieval across the two languages, as defined in the detailed requirements.

## Basic workflow

1. The user submits a draft decision and its relevant details.
2. Explicit organizational rules check the issuing position's permission and allowed scope.
3. When authorization checks permit, the retrieval component finds relevant existing instructions.
4. A local language model analyzes the draft against the retrieved material for potential conflicts.
5. The system presents authorization findings, potential conflicts, explanations, and supporting evidence for human review.
6. The reviewer decides what action to take and may revise and resubmit the draft.

## Project boundaries

- Organizational authorization checks remain separate from AI-based conflict analysis.
- The language model must not invent organizational authority or assume that a higher position automatically grants permission.
- AI processing is intended to run locally within the approved project scope.
- Extracted organizational information requires authorized human review before it becomes active configuration.
- Findings support review and must not be treated as automatic approval or a guarantee that no conflict exists.

## Documentation and folder guide

| File or folder | Purpose |
| --- | --- |
| [AGENTS.md](AGENTS.md) | Instructions for coding assistants working on the project |
| [Project overview](docs/01-project-overview.md) | Detailed project concept and goals |
| [Problem and scope](docs/02-problem-and-scope.md) | Problem definition and project boundaries |
| [Requirements](docs/03-requirements.md) | Functional and non-functional requirements |
| [System architecture](docs/04-system-architecture.md) | Components and data flow |
| [Organizational rules](docs/05-organizational-rules.md) | Roles, permissions, scope, and organizational configuration |
| [AI and RAG](docs/06-ai-and-rag.md) | Retrieval and local AI analysis |
| [Evaluation plan](docs/07-evaluation-plan.md) | Testing approach and evaluation metrics |
| [Decisions](docs/08-decisions.md) | Confirmed design decisions and their reasons |
| [Project status](docs/09-project-status.md) | Progress, current tasks, and next steps |
| [Report 1](reports/report-1.md) | Project Report I |
| [Report 2](reports/report-2.md) | Project Report II |
| [Final report](reports/final-report.md) | Final academic report |
| `src/` | Application source code |
| `tests/` | Test cases |

## Current stage

This folder currently contains the documentation scaffold, this introductory README, and agent instructions. The detailed documentation and report files are placeholders to be populated later with user-provided or approved content. The `src/` and `tests/` folders are currently empty.

The features above describe the intended system; they are not a claim that the prototype has been implemented or evaluated. Detailed requirements and technology choices should be recorded in their designated documents as they are confirmed.
