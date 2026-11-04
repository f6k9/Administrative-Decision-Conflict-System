# ITISAQ — Project Report I

> Markdown transcription of `ITISAQ_Report_C06.pdf` (18 pages). The report wording is preserved; headings, paragraphs, lists, and tables have been formatted for Markdown. Cover logos and printed page numbers are omitted. Statements about progress and model choices reflect this report version.

<!-- Source PDF: page 1 -->

CPCS498 – Project I

King Abdulaziz University

Faculty of Computing and Information Technology

Report Part I

Presented By:

| Student Name | Student ID |
| --- | --- |
| Faris Ahmad Khayat | 2337100 |
| Sulaiman Al-Ahmadi | 2339323 |

Supervisor: Dr. Mohammed Dahab

<!-- Source PDF: page 2 -->

## Question 1: Specific Title and Project Aims

### 1.1 Project Title

ITISAQ: Local LLM Support for Administrative Decision Review

### 1.2 Project Aims

The project aims to develop a software prototype that assists organizational staff while preparing administrative decisions, before they are issued. Users will submit a draft decision, and the system will check the issuer’s permissions and allowed scope, retrieve relevant existing decisions, and identify potential conflicts with supporting explanations.

By bringing relevant instructions and review findings together, ITISAQ aims to reduce the time and effort needed to prepare and review a decision. Its value includes helping users find applicable instructions even when no conflict is detected.

The specific objectives are to:

1. Represent organizational units, positions, reporting relationships, permissions, and allowed scopes in a reviewed JSON configuration.

2. Allow users to submit draft administrative decisions in Arabic and English before issuance.

3. Check whether the issuing position has permission to perform the requested action and whether the draft falls within its allowed scope.

4. Retrieve relevant existing decisions helping users understand the instructions that apply to their draft.

5. Use a local large language model to identify potential conflicts between the draft and applicable existing decisions.

6. Present findings with clear explanations and supporting passages so users can review and revise their draft before issuance.

7. Extract proposed configuration updates from organizational charts and job descriptions, link them to the correct positions, and require human confirmation before use.

8. Evaluate the system’s checks and compare decision preparation and review time and effort with a manual process.

### 1.3 Tangible Project Deliverable

The project will deliver a working software prototype through which users can submit draft decisions, view relevant existing instructions, and receive permission, scope, and potential conflict findings before issuance.

The prototype will include organizational configuration management, decision storage and retrieval, local language model analysis, and an interface for reviewing findings and supporting evidence. Authorized personnel will remain responsible for revising and issuing decisions.

The prototype will be accompanied by a documented test dataset and an evaluation report.

<!-- Source PDF: page 3 -->

## Question 2: The Project Proposal

### 2.1 Problem Definition

Preparing an administrative decision requires understanding the organizational rules and existing decisions that apply to it. Before issuing a new decision, staff must check their authority, identify the people or units affected, and review relevant instructions to avoid introducing conflicting requirements.

Even in an organization with well-managed policies and no known conflicts, this preparation process can require considerable manual work. Relevant information may be distributed across documents, and users must locate, read, and compare it before completing their draft. As the number of decisions grows, this process becomes harder to manage and may lead to repeated corrections or delays.

Potential conflicts cannot be identified through text similarity alone. Two decisions may use similar words but apply to different departments, while differently worded decisions may impose incompatible instructions on the same situation. Identifying a relevant conflict therefore requires considering meaning, actual coverage, effective dates, exceptions, and organizational authority. A lack of permission to issue a decision must also be distinguished from a conflict between decision contents.

This is a non-trivial computer science problem involving document processing, information retrieval, natural language analysis, structured organizational data, and rule-based validation. ITISAQ addresses this problem by supporting decision preparation before issuance and presenting relevant information and potential problems to human reviewers.

### 2.2 Project Type and Scope

ITISAQ is an applied artificial intelligence and software development project. It will produce a local software prototype for preparing and reviewing administrative decisions within a configured organization.

The prototype will include:

- A reviewed organizational configuration containing units, positions, reporting relationships, permissions, and allowed scopes.

- Submission of draft administrative decisions in Arabic and English.

- Permission and scope checks before semantic conflict comparison.

- Storage and retrieval of supplied existing decisions, including their sources, actual coverage, effective dates, and status.

- Local language model analysis of potential conflicts between a draft and relevant existing decisions.

- Results containing explanations, supporting passages, and recommended next steps based on organizational rules.

<!-- Source PDF: page 4 -->

- Proposed configuration updates extracted from text or images of organizational charts and job descriptions, linked to the correct positions and subject to human confirmation.

### 2.3 Target Users

The target users are:

- Decision authors: Staff and managers who prepare draft decisions and need to find relevant instructions before issuance.

- Administrative reviewers: Authorized personnel who verify permissions, examine potential conflicts, and determine the appropriate action.

- Configuration administrators: Personnel responsible for maintaining and confirming organizational structures, permission rules, and reference documents.

The prototype will use a simplified access model that distinguishes these responsibilities.

### 2.4 Suggested Solution

ITISAQ will bring organizational checks and document analysis into one review workflow. Users will submit a draft decision and receive relevant existing instructions, permission and scope findings, and explanations of potential conflicts before issuance.

The system will have two main processes.

#### A. Preparing organizational information

Organizational charts, job descriptions, and official rules will be supplied as text or images. Text extraction, OCR, or a local vision-capable model will be used where appropriate. A local language model will propose structured information and match each extracted description to the relevant position.

The proposed information will be checked for valid structure and reviewed by an authorized person before being saved in the JSON configuration. The system will retain supporting source references and will not treat an unclear responsibility as an established permission.

#### B. Reviewing a draft decision

1. Receive the draft: The user submits the decision text, issuing position, intended action, actual coverage, and relevant dates. Extracted or suggested details are confirmed when needed.

2. Check permission and scope: Python-based rules check whether the position may perform the action and whether the draft stays within its allowed area. A confirmed failure is explained to the user. Missing or ambiguous information is flagged for clarification.

3. Retrieve applicable decisions: For drafts that pass these checks, the system identifies relevant existing decisions using their status, dates, actual coverage, and content.

4. Analyze potential conflicts: The local language model compares the draft with the retrieved instructions. It considers whether they apply to the same situation and impose requirements <!-- Source PDF: page 5 --> that cannot be followed together. Shared coverage alone is not sufficient to establish a conflict.

5. Apply organizational rules and display findings: Explicit rules determine authority relationships and the recommended administrative response. The system presents the result, reasons, supporting text, and any uncertainty for human review.

6. Support revision: Users can revise their draft and submit it again. Authorized personnel remain responsible for the final decision and its issuance.

Decisions from peer departments will not be treated as conflicting when each applies only to its own department. Similarly, a higher organizational rank will not automatically grant every permission or make every conflicting instruction take precedence.

The system remains useful when no conflict is found because it helps users locate applicable instructions and complete routine checks. Any claim of reduced preparation or review time will be evaluated during testing.

### 2.5 Initial Development Activities

| Activity | Planned work and output |
| --- | --- |
| Requirements specification | Define user responsibilities, supported decision categories, required inputs, expected outputs, and functional and non-functional requirements. |
| Data and rule analysis | Prepare the organizational structure, confirm permission and authority rules, examine sample decisions, and define how scope, dates, exceptions, and cancellations will be represented. |
| System design | Design the workflow, JSON schema, decision records, retrieval process, user interface, and result format. |
| Tool and model experiments | Compare candidate local models and retrieval methods on Arabic and English examples, and test document extraction on available hardware. |
| Implementation | Develop organizational configuration management, decision submission, permission and scope checks, retrieval, language model comparison, and result presentation. |
| Testing and evaluation | Evaluate permission and scope checks, retrieval, conflict detection, explanations, and configuration extraction using reviewed reference cases. Compare preparation and review time and effort with a manual process. |
| Documentation and refinement | Document the prototype, address observed weaknesses, and prepare the final demonstration and evaluation findings. |

<!-- Source PDF: page 6 -->

Development will begin with manually reviewed organizational data and text-based decisions. Image extraction and proposed configuration updates will be added after the core decision-review workflow is working, allowing the team to validate the main functionality before expanding the input methods.

## Question 3: Project Schedule

The project is planned across two academic semesters. The first semester will focus on requirements, research, analysis, design, and documentation. The second semester will focus on implementation, testing, evaluation, and final delivery.

The following schedule assumes 16 weeks per semester. Week ranges will be adjusted to the official academic calendar and submission deadlines.

### 3.1 First Semester: Documentation, Analysis, and Design

| Weeks | Stage | Planned Activities | Deliverable or Milestone |
| --- | --- | --- | --- |
| 1–2 | Project definition | Confirm the problem, aims, scope, target users, and expected prototype deliverables with the supervisor. | Agreed project definition and scope. |
| 3–5 | Literature review | Review research on regulatory conflicts, evidence-based language analysis, retrieval, and explicit reasoning. Identify methods and limitations relevant to ITISAQ. | Literature review draft and reference list. |
| 4–6 | Requirements specification | Define user roles, supported decision categories, inputs, outputs, functional requirements, and non-functional requirements. | Reviewed requirements specification and first progress report. |
| 7–9 | Data and rule analysis | Define organizational positions, reporting relationships, permission rules, decision coverage, dates, and status. Prepare sample scenarios covering conflicts, permission failures, and valid decisions. | Initial organizational configuration specification and reviewed sample cases. |
| 10–12 | System design | Design the architecture, JSON schema, decision storage structure, retrieval workflow, interface layouts, and result format. Document local processing and access requirements. | Initial system design and diagrams. |

<!-- Source PDF: page 7 -->

| Weeks | Stage | Planned Activities | Deliverable or Milestone |
| --- | --- | --- | --- |
| 13–14 | Evaluation planning | Define reference-case preparation, evaluation measures, and the planned comparison between manual and system-assisted review. Identify candidate tools and hardware needs. | Evaluation plan and proposed technical options. |
| 15–16 | Review and documentation completion | Consolidate the documentation, resolve supervisor feedback, and refine the implementation plan. Allow time for unfinished tasks and revisions. | Reviewed first-semester documentation and implementation plan. |

The main first-semester milestone is a documented and reviewed design that provides a clear basis for implementation. Requirements and research activities overlap so that findings from the literature can inform the system specification.

### 3.2 Second Semester: Implementation, Testing, and Evaluation

| Weeks | Stage | Planned Activities | Deliverable or Milestone |
| --- | --- | --- | --- |
| 1–2 | Development setup and tool selection | Set up Python and Ollama. Test candidate Arabic–English models on available hardware and select the interface, database, retrieval, and document-reading components. | Working development environment and documented tool choices. |
| 3–4 | Organizational configuration and decision storage | Implement reviewed JSON configuration management and storage of decisions, sources, coverage, dates, and status. Prepare the initial interface for entering drafts. | Working configuration, storage, and draft-submission functions. |
| 5–6 | Permission and scope checks | Implement explicit organizational checks and explanations for permission failures, out-of-scope actions, and missing information. Test them against reviewed cases. | Verified permission and scope checking component. |
| 7–8 | Retrieval and local model integration | Implement retrieval of relevant existing decisions and connect the retrieved passages to the local LLM for conflict analysis. | Working RAG and conflict-analysis workflow. |

<!-- Source PDF: page 8 -->

| Weeks | Stage | Planned Activities | Deliverable or Milestone |
| --- | --- | --- | --- |
| 9–10 | Explained results and human review | Integrate source references, supporting passages, organizational-rule outcomes, uncertainty flags, and draft resubmission into the interface. | Integrated prototype for text-based decision preparation and review. |
| 11–12 | Organizational document extraction | Add text and image processing for charts and job descriptions. Implement position matching, proposed JSON updates, and human confirmation. | Configuration-extraction workflow integrated with the prototype. |
| 11–13 | Testing and evaluation | Evaluate individual components and the complete workflow using separate test cases. Assess Arabic and English results and compare manual review with system-assisted review. | Recorded evaluation results and identified limitations. |
| 14 | Refinement and contingency | Address priority defects, improve weak components, and complete delayed work. Re-test any affected functions. | Stable prototype ready for final delivery. |
| 15–16 | Final documentation and presentation | Complete the implementation and evaluation report, user guidance, demonstration materials, and presentation. | Final prototype, report, and project demonstration. |

### 3.3 Key Milestones

The project will progress through the following milestones:

1. End of Semester 1, Week 6: Reviewed project scope and requirements.

2. End of Semester 1: Completed initial design, evaluation plan, and documentation.

3. End of Semester 2, Week 6: Working organizational data, decision storage, and permission and scope checks.

4. End of Semester 2, Week 10: Integrated text-based decision-review prototype.

5. End of Semester 2, Week 13: Completed planned extraction functionality and recorded evaluation results.

6. End of Semester 2: Final prototype, documentation, and demonstration.

<!-- Source PDF: page 9 -->

### 3.4 Flexibility and Progress Management

The schedule includes time for feedback, revisions, and unexpected delays. First-semester review weeks and second-semester contingency time will accommodate changes without postponing all remaining activities.

Implementation will prioritize the core text-based workflow before image extraction. Manually reviewed organizational data will allow the team to continue developing and testing decision review while document extraction is being completed.

Testing will take place throughout implementation. Formal evaluation cases will remain separate from cases used to adjust prompts or improve the system. Documentation will also be updated during development rather than postponed until the final weeks.

Progress will be reviewed regularly with the supervisor. If model performance, data availability, or hardware constraints affect the schedule, the team will adjust the implementation approach or propose a revised scope for discussion, while maintaining consistency between the agreed requirements and final deliverables.

## Question 4: Literature Search and Bibliography

### 4.1 Literature Search and Selection

The initial targeted search used combinations of “regulatory documents” and “conflict detection”; “document-level natural language inference” and “contracts”; “requirement contradiction detection” and “formal logic”; “retrieval-augmented generation” and “evidence relevance”; and “multilingual text embeddings” and “Arabic retrieval”. Publications were located through web searches and checked on ACL Anthology, Springer Nature, ICLR proceedings, arXiv, and an author-uploaded conference paper. The original search date and result counts were not recorded, so they are not reconstructed here.

A supplementary targeted search and source verification were completed on 10 October 2026. The web-search queries recorded below identify the discovery route; the publication sites are access and verification locations, not evidence that their databases were systematically searched. Google Scholar, Scopus, and Web of Science were not directly searched during this supplementary review.

Organizational charts: “organizational chart extraction hierarchy image research paper”; Sayama and Yamanoi’s full text was inspected on arXiv and its published chapter metadata checked through Waseda University’s research record.

Arabic retrieval: “ArabicMTEB benchmark”; the published Swan and ArabicMTEB paper and metadata were checked through ACL Anthology.

Existing sources were also checked through their publication records and available full texts.

No database date filter or exhaustive result-count procedure was applied. Screening favored scientific papers from 2021–2026 that directly addressed an ITISAQ objective, provided inspectable methods or data, and had identifiable authors and publication/version details. Generic promotional pages, unverifiable claims, and sources without a useful connection to the <!-- Source PDF: page 10 --> proposed workflow were excluded from the scientific evidence base. Publisher or institutional records supplied bibliographic details; The Open University’s guidance supplied methodological context for PROMPT rather than scientific evidence about ITISAQ.

Six scientific publications were retained to cover complementary needs, rather than an arbitrary reference quota. All six were published between 2021 and 2025 and fall within five years of the supplementary search. ContractNLI, published in November 2021, remains within the window. Older work is not used to claim current model performance. The review is targeted, not exhaustive, and findings remain bounded by each source’s task and data.

### 4.2 Literature Review

#### 4.2.1 Conflicts in Organizational Documents

Organizational decisions operate within policies, guidelines, and instructions. Schumann and Marx Gómez (2024) review 46 publications and compare document types, conflict interpretations, and detection approaches. Gärtner and Göhlich (2024), by contrast, analyze contradictions in controlled-language engineering requirements. Together, these sources show why ITISAQ needs an explicit operational definition: apparently incompatible statements matter only when their instructions apply to the same situation.

For ITISAQ, semantic conflict must remain distinct from permission failure. Actual coverage, effective dates, exceptions, and decision status are proposed applicability requirements; decisions confined to different departments should not be labeled conflicting merely because their wording differs. These project-specific rules require reviewed organizational cases and are not established by transferring results from other domains.

#### 4.2.2 Meaning Comparison and Supporting Evidence

Koreeda and Manning (2021) introduce ContractNLI, which evaluates supplied hypotheses against 607 annotated contracts and identifies supporting evidence spans. Its entailment, contradiction, and not-mentioned distinctions connect the broader regulatory-document literature to an inspectable comparison task. Long documents and exceptions remain important difficulties.

ContractNLI and Self-RAG (Asai et al., 2024) address different stages of evidence use: identifying passages that justify a classification and checking whether retrieved context supports generated output. Their combination informs ITISAQ’s presentation of original passages and source references. Neither task establishes organizational authority or discovers every conflict among administrative records; those boundaries require separate checks and test cases.

#### 4.2.3 Explicit Reasoning and Organizational Authorization

ALICE combines formal logic, a decision tree, and LLM responses for contradiction analysis (Gärtner & Göhlich, 2024). Its approach addresses content relationships, while organizational authorization requires separate project-specific checks. This distinction supports ITISAQ’s existing separation between local language analysis and explicit Python checks.

<!-- Source PDF: page 11 -->

A reporting relationship is not itself a permission to perform every action. The configured organization must explicitly define permitted actions, scope, and applicable authority relationships. ITISAQ’s organizational rules must also address decision precedence, exceptions, and delegation where applicable. Similarly, ALICE’s controlled language and formal reasoning cannot be equated with ordinary administrative prose. ITISAQ will validate its reviewed JSON rules and conflict cases independently.

#### 4.2.4 Retrieval and Evidence-Supported Analysis

Asai et al. (2024) introduce Self-RAG, which retrieves when needed and assesses relevance and support using a specialized training approach. In conjunction with ContractNLI, it motivates evaluation of both context selection and the evidence behind findings. ITISAQ’s proposed RAG workflow will preserve source references and use coverage, dates, and status to identify applicable decisions; the initial prototype does not reproduce Self-RAG training.

Retrieval and conflict analysis will be evaluated separately because a missing applicable decision can prevent a correct conflict finding. Conversely, a semantically similar passage does not establish contradiction. The sources support this division of evaluation responsibilities, while the appropriate retrieval method and model remain subject to the project’s initial experiments.

#### 4.2.5 Arabic and English Retrieval

Bhatia et al. (2025) provide evidence with Swan and ArabicMTEB, covering Arabic varieties and multiple embedding tasks. Their results make Arabic-specific evaluation important when considering multilingual candidates; they do not select ITISAQ’s eventual embedding model.

Neither general embedding benchmarks nor multilingual coverage demonstrate accuracy on Arabic administrative permissions, negation, or exceptions. ITISAQ therefore needs its own Arabic and English examples, including differently worded instructions and relevant decisions across languages. Retrieval representations must be combined with metadata applicability checks and subsequent conflict analysis. These are evaluation implications within the existing scope, not additional functionality.

#### 4.2.6 Extracting Organizational Charts and Job Descriptions

Sayama and Yamanoi (2024) reconstruct organization networks by combining chart labels, boxes, and connecting lines. Their work informs ITISAQ’s planned organizational-chart extraction and configuration proposals. Job-description extraction remains a separate proposed project function.

A successfully extracted chart does not prove that every relationship is correct, and information extracted from a job description does not grant administrative authority. This study therefore informs chart-extraction evaluation without validating position matching, job-description extraction, or Arabic permission extraction. ITISAQ’s existing human-confirmation step remains necessary before proposed updates enter its reviewed configuration. Chart relationships, textual fields, and their assignment to positions will require separately reviewed examples; the study does not justify adopting a particular extraction tool.

<!-- Source PDF: page 12 -->

#### 4.2.7 Human Review and Efficiency Evaluation

ContractNLI and Self-RAG support the use of inspectable evidence, but an explanation alone does not establish that users will make better decisions.

For ITISAQ’s existing evaluation objective, manual and system-assisted preparation should be compared on reviewed cases while recording correctness, preparation/review time, and perceived effort. Comparable case difficulty and controlled task order can limit learning effects. Results must report whether any time saving accompanies preserved decision quality. These are proposed evaluation choices, not results of the cited studies or a promise of improvement. No additional cognitive-forcing interface functionality is committed.

#### 4.2.8 Implications for ITISAQ

The retained literature informs applicable-document retrieval, meaning comparison, evidence presentation, and organizational-chart extraction. ITISAQ combines these ideas with its own requirements for organizational authorization and human review during decision preparation before issuance, retaining its reviewed configuration, local analysis, and human responsibility. Finding applicable instructions remains useful even when no conflict is detected.

No selected study validates this entire integration. Permission and scope checks, retrieval, conflict findings, explanation quality, configuration extraction, and preparation time require ITISAQ-specific evaluation. Evidence remains limited for Arabic administrative authority language and reliable matching of extracted descriptions to the configured positions. These limitations motivate domain testing and further targeted reading without changing the project’s agreed aims, functionality, or schedule.

### 4.3 Source Evaluation Using PROMPT

The following evaluations explicitly apply the supplied assignment Table 1: Presentation, Relevance, Objectivity, Method, Provenance, and Timeliness. These dimensions also appear in The Open University’s (n.d.) PROMPT guidance. Presentation considers clarity, figures, audience, and prerequisite knowledge; relevance identifies the project need; objectivity examines the authors’ perspective and reasons for confidence; method considers data collection and validity; provenance identifies origin and publication; and timeliness considers dates, versions, and continuing usefulness.

The judgments below support use for stated purposes, not blanket certification. Identifiable venues and academic or corporate affiliations improve traceability but do not guarantee independence or reliability. Where funding or competing-interest information is not established, neutrality is not assumed. No source alone establishes ITISAQ performance.

#### 4.3.1 Schumann and Marx Gómez (2024)

Presentation: Selection diagrams and thematic comparisons clarify the review; readers need basic NLP and rule-analysis knowledge.

Relevance: Directly informs regulatory-conflict definitions; useful background rather than a validated administrative prototype.

<!-- Source PDF: page 13 -->

Objectivity: Oldenburg researchers synthesize multiple approaches and limitations; English-only selection constrains the perspective.

Method: Six search services, stated exclusions, and citation tracing yield 46 papers. Transparent selection supports scrutiny, but coverage is not universal.

Provenance: IDSTA 2024 IEEE conference paper; identifiable authors and DOI. The inspected full text is author-uploaded, not a publisher-hosted copy.

Timeliness: Published in 2024; useful recent background, but its search coverage cannot establish the state of all subsequent research.

Suitability: Retain for problem framing; validate the adopted conflict definition on organizational examples.

#### 4.3.2 Koreeda and Manning (2021)

Presentation: Task labels and evidence examples are clear; model details require familiarity with document-level NLI.

Relevance: Strong reference for evidence-backed classification; contract hypotheses differ from administrative decision pairs.

Objectivity: The authors propose a dataset and baseline but disclose difficult cases and remaining weaknesses, allowing their claims to be examined.

Method: Annotated contracts and comparative model evaluation provide inspectable evidence. Annotation judgments and contract-domain coverage limit transfer.

Provenance: Published in Findings of EMNLP 2021; ACL supplies the paper, authors, page range, and DOI.

Timeliness: November 2021 is within five years of this review. Retain the task design; do not treat its baseline as current model performance.

Suitability: Retain for inference and evidence evaluation, with separate administrative reference cases.

#### 4.3.3 Gärtner and Göhlich (2024)

Presentation: The contradiction taxonomy and decision tree organize the argument; formal logic knowledge is needed to interpret the method.

Relevance: Supports explicit reasoning alongside LLM analysis; controlled engineering requirements differ from organizational prose.

Objectivity: The authors evaluate their own ALICE system against an LLM-only approach; comparisons and reported limitations permit scrutiny without proving independence.

Method: Specified reasoning steps and comparative experiments support assessment. Language restrictions and evaluation data constrain generalization.

Provenance: Automated Software Engineering, volume 31, Article 49; Springer hosts the identifiable authors and full article with DOI.

<!-- Source PDF: page 14 -->

Timeliness: Published 6 June 2024. Its reasoning structure remains relevant, while model-dependent results require fresh local testing.

Suitability: Retain as a reasoning reference; do not equate its reported performance with ITISAQ accuracy.

#### 4.3.4 Asai et al. (2024)

Presentation: Framework diagrams and experiments explain retrieval and reflection; training notation requires LLM knowledge.

Relevance: Useful for passage relevance and evidence support, although ITISAQ does not reproduce its training pipeline.

Objectivity: University, AI-institute, and IBM affiliations are disclosed. The authors evaluate their own framework; baselines provide context rather than independent replication.

Method: Benchmark comparisons and ablations make the approach testable. They concern generation tasks, not organizational conflict or permission checking.

Provenance: Published ICLR 2024 paper available through official proceedings; publication year is distinguished from the earlier preprint.

Timeliness: The 2024 publication remains relevant to retrieval-supported evidence analysis; specific model rankings are time-sensitive.

Suitability: Retain for retrieval/evidence evaluation; confirm relevance on ITISAQ decisions and available hardware.

#### 4.3.5 Sayama and Yamanoi (2024)

Presentation: Stepwise illustrations make chart reconstruction understandable; image-processing and graph knowledge are needed.

Relevance: Directly addresses organization-chart extraction; it does not determine permissions or validate Arabic charts.

Objectivity: The authors present their own heuristics and acknowledge failed layouts; absence of a competing-method comparison weakens performance claims.

Method: Published Japanese chart data and extraction steps are identifiable. A 46% acquisition rate is not node/relationship accuracy or proof of generalization.

Provenance: Springer IDSCS proceedings chapter, verified through Waseda’s record; full text was inspected in the corresponding 2023 arXiv version.

Timeliness: Published in 2024, using 2008–2011 charts; older source layouts may not represent current inputs.

Suitability: Retain for extraction design and limitations; review recovered labels and relationships before configuration use.

<!-- Source PDF: page 15 -->

#### 4.3.6 Bhatia et al. (2025)

Presentation: Benchmark organization and task tables clarify Arabic coverage; interpretation requires embedding-evaluation knowledge.

Relevance: Provides Arabic-specific benchmark evidence, without validating administrative conflict analysis.

Objectivity: The same research team proposes models and the benchmark. Explicit discussion of synthetic-data bias supports critical reading but not independence.

Method: Multi-task and cross-language evaluation is broader than a single test; dataset composition and synthetic data limit domain transfer.

Provenance: Published in Findings of NAACL 2025; ACL supplies the scientific paper, authors, metadata, and DOI.

Timeliness: Published in April 2025; evolving model performance still requires local comparison.

Suitability: Retain for Arabic retrieval evaluation; assess formal administrative language on reviewed project examples.

The sources have the following principal boundaries:

| Source | Important Limitation for ITISAQ |
| --- | --- |
| Schumann and Marx Gómez (2024) | A review of varied approaches, rather than validation of one administrative decision-support system. |
| Koreeda and Manning (2021) | A contract inference task, without organizational permission and authority checks. |
| Gärtner and Göhlich (2024) | Controlled-language engineering requirements, with results dependent on the tested methods and datasets. |
| Asai et al. (2024) | A specialized retrieval-and-generation framework, rather than an administrative conflict-detection system. |
| Sayama and Yamanoi (2024) | Heuristic extraction on Japanese charts; acquisition success does not establish relationship accuracy or Arabic applicability. |
| Bhatia et al. (2025) | Arabic-centric embedding benchmarks that do not establish performance on administrative permissions, negation, exceptions, or ITISAQ-specific retrieval tasks. |

Taken together, the sources satisfy the purpose of a critically selected initial evidence base, with explicit methodological and transfer limits. None guarantees ITISAQ reliability. Model choices, authority rules, extraction outputs, and human-review benefits remain subject to the evaluation described in the proposal.

<!-- Source PDF: page 16 -->

### 4.4 References

Asai, A., Wu, Z., Wang, Y., Sil, A., & Hajishirzi, H. (2024). Self-RAG: Learning to retrieve, generate, and critique through self-reflection. In Proceedings of the Twelfth International Conference on Learning Representations. https://proceedings.iclr.cc/paper_files/paper/2024/file/25f7be9694d7b32d5cc670927b8091e1-Paper-Conference.pdf

Bhatia, G., Nagoudi, E. M. B., El Mekki, A., Alwajih, F., & Abdul-Mageed, M. (2025). Swan and ArabicMTEB: Dialect-aware, Arabic-centric, cross-lingual, and cross-cultural embedding models and benchmarks. In L. Chiruzzo, A. Ritter, & L. Wang (Eds.), Findings of the Association for Computational Linguistics: NAACL 2025 (pp. 4669–4685). Association for Computational Linguistics. https://doi.org/10.18653/v1/2025.findings-naacl.263

Gärtner, A. E., & Göhlich, D. (2024). Automated requirement contradiction detection through formal logic and LLMs. Automated Software Engineering, 31, Article 49. https://doi.org/10.1007/s10515-024-00452-x

Koreeda, Y., & Manning, C. D. (2021). ContractNLI: A dataset for document-level natural language inference for contracts. In M.-F. Moens, X. Huang, L. Specia, & S. W.-t. Yih (Eds.), Findings of the Association for Computational Linguistics: EMNLP 2021 (pp. 1907–1919). Association for Computational Linguistics. https://doi.org/10.18653/v1/2021.findings-emnlp.164

Sayama, H., & Yamanoi, J. (2024). Extracting network structures from corporate organization charts using heuristic image processing. In S. Shukla, H. Sayama, J. V. Kureethara, & D. K. Mishra (Eds.), Data science and security: Proceedings of IDSCS 2023 (pp. 61–70). Springer. https://doi.org/10.1007/978-981-97-0975-5_5

Schumann, G., & Marx Gómez, J. (2024). Detection of conflicts, contradictions and inconsistencies in regulatory documents: A literature review. In 2024 Fifth International Conference on Intelligent Data Science Technologies and Applications (IDSTA). IEEE. https://doi.org/10.1109/IDSTA62194.2024.10747003

<!-- Source PDF: page 17 -->

## Question 5: Equipment or Software Used

### 5.1 Equipment

Development and local testing will use the most capable personal computer available to the team. Its processor, RAM, available graphics hardware, and storage capacity will guide the model configuration and the amount of data processed locally. Storage will be needed for model files, project documents, the decision collection, and test results.

### 5.2 Main Software

Python will be used to implement the system logic, organizational permission and scope checks, document-processing workflow, and integration of the system components. Ollama will be used to run the local language model and connect it to the Python application.

Gemma (`gemma4:12b`) and Qwen (`qwen3.5:9b-q4_K_M`) have been shortlisted as candidate local language models following preliminary testing on Arabic and English datasets. Gemma currently shows stronger overall performance in our administrative decision tests, while Qwen remains a comparison candidate. The final selection will consider further evaluation, Arabic and English performance, response time, and the available hardware.

### 5.3 Supporting Software and Project Resources

The project will also need a user-interface framework and a database or local storage solution. An embedding model and a vector store will support retrieval-augmented generation (RAG) by indexing decision passages and retrieving relevant existing decisions for Arabic and English inputs. Retrieval will consider decision scope, effective dates, and status before the local language model checks for possible conflicts. Document-reading tools, will support the planned extraction of information from organizational charts and job descriptions. JSON will store the reviewed organizational structure and permission rules.

<!-- Source PDF: page 18 -->

## Question 6: Work Intended in the Near Future

During the next stage of the project, we intend to build on the model testing already started. Our immediate priorities are to document the model comparison, prepare test cases relevant to ITISAQ, and develop a small working prototype.

### 6.1 Complete and Document the Model Comparison

We will continue testing Gemma, Qwen and the other candidate models using the same datasets and test conditions. We will document answer accuracy against expected responses, Arabic-language handling, and response time on the available personal computer. This is a priority because Gemma is currently the preferred candidate, and a consistent comparison will help confirm whether it meets the project’s needs. The resulting record will support the choice of model and configuration before further integration.

### 6.2 Prepare Test Cases Relevant to ITISAQ

We will prepare a manageable set of cases involving administrative decisions, organizational permissions, and job responsibilities. The team will review the expected responses against the organizational information supplied for each case. These cases will help assess whether the system identifies relevant conflicts and provides supporting evidence. This work is a priority because performance on general datasets does not establish suitability for ITISAQ’s tasks. The reviewed cases will provide a basis for checking the prototype and identifying errors that require further investigation.

### 6.3 Develop a Small Working Prototype

Using Python and Ollama, we will build an initial workflow that processes an administrative decision, connects it to relevant organizational information, and presents the result and supporting evidence for human review. We will test this workflow with the prepared cases and record incorrect outputs and integration problems. This is a priority because it will reveal practical issues in local model operation and the connection between system components before broader implementation. The prototype will guide subsequent development while keeping the project’s existing aims and scope.
