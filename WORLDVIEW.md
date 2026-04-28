# Project Worldview (WORLDVIEW.md)

## Purpose

- `WORLDVIEW.md` defines this project's worldview: shared meaning, ontology, axioms, epistemic guidance, and evaluation outputs that AI Harness sessions and Developers use to reason consistently about the project.
- AI Harness sessions consume this file when interpreting project terms, classifying artifacts, evaluating claims for truth, and resolving ambiguity in specs, code, summaries, and Agent-to-Developer replies.
- Developers consume this file to align human and Agent vocabulary so that decisions, reviews, and handoffs use the same words for the same things.

## Scope

- `WORLDVIEW.md` defines what project concepts mean, what entities exist, how they relate, which stable invariants hold, and how project claims are evaluated.
- `WORLDVIEW.md` does not define operational actions, workflow routing, approval gates, task procedures, or tool permissions — those belong in `RULES.md`.
- `WORLDVIEW.md` does not define session loading discipline, Agent behavior, or platform-specific configuration — those belong in `AGENTS.md` and platform entry points.

## Automation Program

### Domain Boundary

- **Purpose:** Covers the meaning of the RISE Automation Program — its mission, the five program functions, the artifacts that flow through it (opportunities, initiatives, KPIs), and how those artifacts relate to RISE's business.
- **In scope:** Program functions, automation maturity assessment, opportunities, initiatives, roadmap items, KPIs, and the knowledge base content that records all of the above.
- **Out of scope:** RISE's customer-facing fiber ISP products (dedicated/shared business internet, EVPL, IP Transit, GetaFIX, Teleport, colocation) and external sales/marketing concepts — those belong to RISE's product domain, not this program.

### Terminology

- **Automation Program:** A Technology-department program at RISE whose mission is to build digital intelligence infrastructure (automation + business intelligence + network intelligence) so RISE can operate at scale with precision and agility.
- **Program Function:** One of the five named responsibilities of the Automation Program — Strategy & Roadmap Development, Opportunity Identification & Development, Initiative Management & Cross-Functional Execution, Governance Standards & Reusability, and Performance Tracking & Continuous Improvement.
- **Opportunity:** A discovered and evaluated chance to improve operational efficiency, service quality, or sustainability through automation. Opportunities are inputs to initiatives.
- **Initiative:** An approved opportunity translated into structured execution work, coordinated cross-functionally to deliver measurable outcomes.
- **Roadmap:** A phased plan that progressively develops the organization's automation capability and capacity, anchored to a defined target vision.
- **Maturity Assessment:** An evaluation of RISE's current state of automation capability used as the baseline for the roadmap.
- **Objective:** A defined outcome within an Initiative — a specific, measurable result scoped to 1-2 quarters. Owned by an Objective Lead and defined together with one or more Key Results. Objectives are planned into Annual Roadmaps and tracked in the Operational Roadmap.
- **Key Result:** A measurable outcome that defines whether an Objective has been met. Defined alongside its Objective. Where a KPI is defined for the area, Key Results may set or change KPI targets.
- **KPI:** A defined performance measure (cost savings, efficiency gains, error reduction) used to track impact in a domain. Where a KPI is defined for an area, Key Results may set or change its target.
- **Process:** One of three named program processes recorded in `program-files/about/Program Processes.md` — Strategy, Develop, Org Dev — that govern how Objectives, Work Items, and change-management efforts move through the Automation Program.
- **Strategy Process:** Process that works on Objectives through stages: Intention → Develop → Active → Done → Archived. Tracked in the AUTO project Jira timeline.
- **Develop Process:** Process that develops an Idea to a business Impact through stages: Idea → Opportunity → Analysis → Planning → Implementation → Review → Done → Archived. Tracked in program work boards (EA, BI, NI, etc.).
- **Org Dev Process:** Supporting change-management process applied case-by-case (stakeholder alignment, training, communication, role redesign). Currently in early stages.
- **Work Item:** An individual unit of work that contributes to an Objective. Tracked on a Work Board and linked to its parent Objective in the Operational Roadmap. Has four kinds: Story, Study, Task, Workstream.
- **Story:** A discrete feature or enhancement built into an application. Flows through all Develop stages and produces a deployable deliverable.
- **Study:** An analytical effort to explore an idea or opportunity and produce a recommendation or decision. Typically concludes at Analysis.
- **Task:** A general-purpose Work Item for data operations, maintenance, or other activities not qualifying as a Story or Study.
- **Workstream:** A grouping container that bundles related Work Items under a shared purpose. Does not flow through Develop stages itself; provides traceability across the Stories, Studies, and Tasks within it.
- **Program Manager:** Role accountable for defining and maintaining the Program roadmap, evaluating ideas/opportunities, monitoring program health, and evolving the program's processes.
- **Objective Lead:** Role accountable for an Objective — milestone breakdown, schedule, forward progress, and posting status updates in the roadmap board.
- **Development Lead:** Role accountable for a Work Item — task breakdown, schedule, forward progress, and posting updates in the program work board.
- **Knowledge Base (KB):** The Markdown content under `docs/kb/` that records program context, decisions, and reference material. KB content is internal — it is not published to external surfaces.
- **Sub-Program:** A strategic focus area within the Automation Program, recorded under `program-files/programs/<sub-program>/`. Currently four: Artificial Intelligence, Business Intelligence, Enterprise Automation, and Network Intelligence. Each Sub-Program has its own goals and may produce its own Opportunities, Initiatives, and KPIs. Published to the Astro site and Confluence, and co-edited via Google Docs.
- **Internal Program:** A cross-cutting operational program supporting the Automation Program, recorded at the top level of `program-files/<internal-program>/` (not under `programs/`). Currently two: Framework and Architecture (enterprise standards for IT use cases, information models, terminologies, and architecture) and Upkeep (maintenance, major repair, and decommission of program implementations). Published to the Astro site and Confluence, and co-edited via Google Docs.
- **Mission:** The Automation Program's stated purpose, recorded in `program-files/Mission.md`. Published to the Astro site and Confluence, and co-edited via Google Docs. The Roadmap, Sub-Programs, and Internal Programs derive their direction from the Mission.
- **Analysis Document:** A research or data-analysis document recorded under `program-files/analysis/<year>/` that supports decision-making for the Automation Program (e.g., system-decommission analyses).
- **About Document:** A descriptive context document recorded under `program-files/about/` that introduces RISE, the Automation Program, or its key management activities.
- **Initiative Document:** A Markdown file that records a single Initiative, including its purpose, leads, working group, objectives, and history. Recorded under `program-files/programs/<sub-program>/initiatives/<initiative>.md` for Sub-Program initiatives or `program-files/<internal-program>/initiatives/<initiative>.md` for Internal Program initiatives.
- **Roadmap Document:** A Markdown file that records a Roadmap (typically year-scoped). Recorded under `program-files/roadmap/<year>/<roadmap>.md`.
- **Roadmap Kind:** One of four named roadmap views per `Work Management.md` — Annual Roadmap (yearly plan), Operational Roadmap (live Jira-tracked execution view), Program Roadmap (initiatives within a program), Initiative Roadmap (objectives within an initiative).
- **Strategy Document:** A document recorded under `program-files/strategy/` that expresses program-level strategic stance (e.g., Values and Principles).
- **Working Group:** A long-lived virtual team formed around a system domain (BSS, OSS, BI, NI), spanning Initiatives. Recorded in `program-files/work-system/Working Groups.md`.
- **Work Board:** A Jira board used to track work items within an Initiative or program. Indexed in `program-files/work-system/Work Boards.md`.
- **Collaboration Channel:** A Slack channel used for program, initiative, project, or operational collaboration. Indexed in `program-files/work-system/Collaboration Channels.md`.
- **Wiki-link:** A frontmatter field (`Wiki-link: <url>`) on a `program-files/` Markdown file that points to the corresponding Confluence page. The frontmatter is local-only metadata; it is stripped before publishing to Confluence.

### Ontology

- **Class: Program** — The Automation Program itself. The project owns exactly one.
- **Class: Sub-Program** — A strategic focus area within the Program. Currently four instances: Artificial Intelligence, Business Intelligence, Enterprise Automation, Network Intelligence. Recorded under `program-files/programs/<sub-program>/`.
- **Class: Internal Program** — A cross-cutting operational program supporting the Automation Program. Currently two instances: Framework and Architecture, Upkeep. Recorded at the top level of `program-files/<internal-program>/` (not under `programs/`).
- **Class: Function** — A Program Function (one of the five). Belongs to the Program.
- **Class: Opportunity** — Belongs to a Function (typically Opportunity Identification & Development) and is associated with a Sub-Program or Internal Program.
- **Class: Initiative** — Derived from an approved Opportunity. Owned by Initiative Management & Cross-Functional Execution; tagged to its Sub-Program or Internal Program.
- **Class: Objective** — Belongs to an Initiative. Owned by an Objective Lead. Recorded within the Initiative Document.
- **Class: Key Result** — Belongs to an Objective. Measures outcome; may set KPI targets where a KPI is defined.
- **Class: KPI** — Attached to an Initiative or domain; rolls up to Performance Tracking & Continuous Improvement.
- **Class: Process** — One of three: Strategy, Develop, Org Dev.
- **Class: Work Item** — Tracked on a Work Board; contributes to an Objective. Has four kinds: Story, Study, Task, Workstream.
- **Class: Role** — A program-management responsibility. Three named instances: Program Manager, Objective Lead, Development Lead.
- **Class: Roadmap Item** — Owned by Strategy & Roadmap Development; sequences Initiatives over time.
- **Class: Mission** — The Program's stated purpose. Exactly one, recorded in `program-files/Mission.md`.
- **Class: Analysis Document** — Research or data-analysis artifact under `program-files/analysis/<year>/` that supports Program decisions.
- **Class: About Document** — Descriptive context artifact under `program-files/about/` that introduces RISE, the Program, or its key activities.
- **Class: Initiative Document** — Markdown artifact that records a single Initiative. Recorded under `program-files/programs/<sub-program>/initiatives/<initiative>.md` for Sub-Program initiatives or `program-files/<internal-program>/initiatives/<initiative>.md` for Internal Program initiatives.
- **Class: Roadmap Document** — Markdown artifact under `program-files/roadmap/<year>/<roadmap>.md` that records a Roadmap. Has four kinds: Annual, Operational, Program, Initiative.
- **Class: Strategy Document** — Markdown artifact under `program-files/strategy/` that expresses program-level strategic stance.
- **Class: Working Group** — Virtual team scoped to a system domain. Recorded in `program-files/work-system/Working Groups.md`.
- **Class: Work Board** — Jira board tracking work items. Indexed in `program-files/work-system/Work Boards.md`.
- **Class: Collaboration Channel** — Slack channel for program collaboration. Indexed in `program-files/work-system/Collaboration Channels.md`.
- **Class: KB Page** — Internal Markdown artifact under `docs/kb/`. May describe any of the above classes. Not published.
- Program → contains → Sub-Programs and Internal Programs.
- Program → produces → Roadmap (via Strategy & Roadmap Development); recorded as Roadmap Documents.
- Function → discovers → Opportunity → becomes → Initiative → carries → Objectives → measured by → Key Results → may set → KPI targets.
- Sub-Program and Internal Program → scope → Opportunities, Initiatives, KPIs; each owns Initiative Documents under its `initiatives/` subdirectory.
- Initiative → recorded in → Initiative Document.
- Working Group → resources → Initiatives.
- Strategy Process → governs → Objective lifecycle (Intention → Develop → Active → Done → Archived).
- Develop Process → governs → Work Item lifecycle (Idea → Opportunity → Analysis → Planning → Implementation → Review → Done → Archived).
- Work Item → contributes to → Objective; → tracked on → Work Board.
- Workstream → groups → Work Items.
- Program Manager → manages → Program; Objective Lead → owns → Objective; Development Lead → owns → Work Item.
- Work Board → tracks → Work Items belonging to Initiatives.
- Collaboration Channel → enables → collaboration on Programs, Initiatives, or operations.
- Mission → anchors → Program direction; Sub-Programs, Internal Programs, Roadmap, and Strategy Documents derive from it.
- Analysis Document → informs → Opportunity, Initiative, or Roadmap Item.
- About Document → describes → Program or RISE context.
- Strategy Document → expresses → Program values and principles.
- KB Page → records → any class above (internal use only).

### Axioms

- The Automation Program serves RISE's Technology department; it is not a customer-facing program.
- Initiatives are derived from approved Opportunities — an Initiative without a corresponding Opportunity is incomplete.
- Initiatives carry one or more Objectives; each Objective is defined with one or more Key Results. Where a KPI is defined for the area, Key Results may set or change KPI targets.
- Performance claims must reference a Key Result (and a KPI target where applicable); claims without a Key Result are `missing`.
- The Roadmap reflects the current Maturity Assessment plus the target vision; changes to either propagate to the Roadmap.
- Governance, Standards & Reusability constrains all other Functions — reusable frameworks and standards take precedence over one-off solutions.
- `program-files/` (Mission and Sub-Program documents) is the system of record for what is published; downstream publishing (Astro, Confluence) and Google Docs co-editing reflect `program-files/`, not the other way around. The Knowledge Base under `docs/kb/` is internal context and is not published.

### Epistemology

- A claim about a Program Function is supported when it cites `program-files/about/About Automation Program.md` or a successor About Document that defines the function.
- A claim about an Initiative is supported when an Initiative Document under `program-files/<program>/initiatives/` records it; absent that, a KB page or workflow artifact may support the claim, otherwise the claim is `missing`.
- A claim about an Opportunity is supported only when a KB page or workflow artifact records it; otherwise the claim is `missing`.
- A claim about a Roadmap is supported when a Roadmap Document under `program-files/roadmap/<year>/` records it; the Operational Roadmap kind additionally references the live Jira board for in-flight status.
- A claim about an Objective is supported when the parent Initiative Document records it (with associated Key Results).
- A claim about a Work Item is supported by a corresponding entry on a Work Board (Jira); absent a board entry, the claim is `missing`.
- A claim about a Process stage transition is supported when the Strategy Process (for Objectives) or Develop Process (for Work Items) reflects it.
- A KPI value is supported only when its definition and measurement source are both recorded; a number without a defined measurement is `unknown`.
- A Key Result is supported only when its target and measurement source are both recorded; a Key Result without a target is `unknown`.
- Conflicts between `program-files/` content and downstream published copies (Astro, Confluence) resolve in favor of `program-files/` until reconciled explicitly. For Google Docs (co-edited), conflicts must be resolved with explicit developer direction since the sync is bidirectional.
- Absence of a KB page about a topic is `missing`, not `false` — the program may simply not have addressed it yet.

### Evaluation Outputs

- **supported:** A KB page or workflow artifact records the claim and its derivation.
- **missing:** No KB page or workflow artifact records the claim yet.
- **unknown:** Artifacts exist but cannot be interpreted confidently (e.g., a KPI number with no measurement definition).
- **conflicted:** `program-files/` content and a downstream published or co-edited copy (Astro, Confluence, Google Docs) disagree and the source of truth has not yet been reconciled.

## Automation Program Platform Development

### Domain Boundary

- **Purpose:** Covers the meaning of the platform that supports the management of the Automation Program — the repository itself, its AIDE-based AI Harness configuration, the program-files and knowledge base directories, architecture docs, and design patterns that together make program-management tasks operable by Developers and Agents. The Platform assists rather than replaces program management; managing the Program remains a human-led activity that the Platform automates routine portions of.
- **In scope:** AIDE components (agents, skills, plugins, hooks, output styles), project entry files (`AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, `CLAUDE.md`, `GEMINI.md`), platform documentation (`docs/architecture/`, `docs/patterns/`), the knowledge base directory (`docs/kb/`) and program-files directory (`program-files/`) as hosted content surfaces, and the pipelines that publish `program-files/` to Astro and Confluence and synchronize them with Google Docs.
- **Out of scope:** Program semantics of KB content (Opportunities, Initiatives, KPIs) — those belong to the Automation Program domain. RISE's customer-facing products are also out of scope.

### Terminology

- **Platform:** The `automation-program` repository plus its AIDE configuration, treated as a single deployable unit. An AI-assisted environment that supports program-management work by automating routine tasks (writing/maintaining opportunity docs, roadmap, analysis) and integrating with Confluence, Jira, and Google Docs for collaboration with program participants.
- **AIDE:** The AI-assisted Development Environment framework that organizes the Platform's Agent-facing configuration into typed components, with shared canonical sources under `.agents/` and platform-specific entry points under `.claude/`, `.gemini/`, `.github/agents/`, and `.codex/agents/`.
- **AIDE Component:** An agent, skill, plugin, hook, or output style installed into the Platform.
- **Canonical Skill:** A skill stored under `.agents/skills/` that is shared across AI Harness platforms via symlinks or platform-specific references.
- **Project Entry File:** One of `AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, or the platform wrappers `CLAUDE.md` and `GEMINI.md` that bootstrap an AI Harness session.
- **Architecture Doc:** A Markdown file under `docs/architecture/` that records Platform structure, integration points, or deployment topology.
- **Design Pattern:** A reusable solution recorded under `docs/patterns/` describing how a recurring Platform problem should be solved.
- **Publishing Pipeline:** Content management scripts that transform `program-files/` artifacts (Mission, Sub-Programs) into the Astro site and Confluence pages (one-way), and synchronize them with Google Docs (bidirectional, via the Google Drive MCP). KB content under `docs/kb/` is not part of the Publishing Pipeline.

### Ontology

- **Class: Platform** — The repository as a whole. Exactly one per project.
- **Class: AIDE Component** — An agent, skill, plugin, hook, or output style. Belongs to the Platform.
- **Class: Project Entry File** — A bootstrap Markdown file (`AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, `CLAUDE.md`, `GEMINI.md`).
- **Class: Architecture Doc** — Markdown artifact under `docs/architecture/`.
- **Class: Design Pattern** — Markdown artifact under `docs/patterns/`.
- **Class: KB Directory** — `docs/kb/`, an internal hosted content surface; its pages are KB Pages in the Automation Program domain. Not published.
- **Class: Program-Files Directory** — `program-files/`, the hosted content surface for program-of-record artifacts (Mission, Sub-Programs); the source for the Publishing Pipeline.
- **Class: Publishing Pipeline** — Scripted transform from `program-files/` to Astro and Confluence (one-way), and bidirectional sync with Google Docs.
- Platform → contains → AIDE Components, Project Entry Files, Architecture Docs, Design Patterns, KB Directory, Program-Files Directory.
- Project Entry File → loads → AIDE Components into an AI Harness session.
- Architecture Doc → describes → Platform structure; Design Pattern → constrains → AIDE Component implementation.
- Publishing Pipeline → reads → Program-Files Directory → writes → Astro, Confluence (one-way); syncs ↔ Google Docs (bidirectional).

### Axioms

- The Platform serves the Automation Program; Platform changes that do not advance program operability are out of scope.
- Canonical Skills under `.agents/skills/` are the source of truth; platform-specific skill directories are references, not forks.
- `AGENTS.md` is the vendor-neutral entry point; `CLAUDE.md` and `GEMINI.md` are thin wrappers that import it.
- Architecture Docs describe the Platform; they do not encode program semantics or operating rules — those live in `WORLDVIEW.md` and `RULES.md` respectively.
- Design Patterns express reusable structure; a one-off implementation that diverges from a recorded Pattern requires explicit justification.
- The Publishing Pipeline reads from `program-files/`, never from `docs/kb/`. Astro and Confluence outputs are one-way (external edits there are not pulled back without an explicit reconciliation step). Google Docs sync is bidirectional and requires explicit developer direction to resolve conflicts.

### Epistemology

- A claim about Platform structure is supported when it cites an Architecture Doc under `docs/architecture/` or the live file layout it describes.
- A claim about an AIDE Component's behavior is supported when it cites the component file itself under `.agents/`, `.claude/`, `.gemini/`, `.github/agents/`, or `.codex/agents/`.
- A claim about a Design Pattern is supported only when a file under `docs/patterns/` records the pattern; otherwise the claim is `missing`.
- Conflicts between a Project Entry File and a platform wrapper resolve in favor of the file the wrapper imports (e.g., `CLAUDE.md` imports `AGENTS.md` — `AGENTS.md` wins).
- Absence of an Architecture Doc or Design Pattern is `missing`, not `false` — the Platform may simply not have recorded that structure yet.

### Evaluation Outputs

- **supported:** A Project Entry File, AIDE Component, Architecture Doc, or Design Pattern records the claim.
- **missing:** No Platform artifact records the claim yet.
- **unknown:** Platform artifacts exist but cannot be interpreted confidently (e.g., a canonical skill referenced from multiple platforms with diverging contents).
- **conflicted:** A Project Entry File and a platform wrapper, or a canonical skill and a platform reference, disagree and the source of truth has not yet been reconciled.

## Management Instructions

> [!IMPORTANT]
> `WORLDVIEW.md` is the authoritative source for project-wide meaning. AI Harness sessions MUST adopt its terms, domains, ontology, relations, axioms, epistemic guidance, and evaluation outputs in artifacts, summaries, and code comments.

### Source-Trust Principles

- Project rules outrank inferred convention.
- Explicit Developer direction governs current-session intent unless it conflicts with repository rules or safety constraints.
- Source files outrank stale summaries of those files.
- Documentation supports interpretation, but it does not override explicit rules or active workflow instructions.

### Epistemic Principles

- Raw input from any party, tool, or file is an assertion until checked against project context.
- Missing information remains unknown; do not treat absence as false or as permission to invent a value.
- Unknown is not true.
- Confidence is not authority.
- Conflict must be explicit.
- Undefined concepts remain undefined until approved.
- Derived values require defined derivation rules and supported inputs.

### Evaluation Outputs

- **supported:** Evidence in project context supports the statement.
- **missing:** Required evidence or context is absent.
- **unknown:** Evidence exists but cannot be interpreted confidently.
- **conflicted:** Project sources or instructions disagree in a material way.
- **not applicable:** The concept or rule does not apply to the current scope.

### Worldview Shape

- Use domain-first organization: Purpose, Scope, one H2 per project domain, then Management Instructions.
- Inside each domain, use the six required H3 subsections in this exact order: Domain Boundary, Terminology, Ontology, Axioms, Epistemology, Evaluation Outputs.
- Each subsection MUST start with at least two concrete entries. Do not ship empty H3 stubs or filler bullets.
- Keep Domain Boundary entries to concise Purpose, In scope, and Out of scope bullets.

### Statement Format

- Prefer one concise statement per bullet over explanatory paragraphs.
- Keep each worldview statement to no more than 100 words.
- Optional clause IDs such as `WV-001` MAY be used for traceability when a statement is referenced from other artifacts; they are NOT required on every entry.
- Use `Clarification:` text only when it adds real disambiguation.

### Adding Statements

- Add worldview statements only for recurring project-wide concepts, artifact classes, workflow states, relations, epistemic guidance, or invariants.
- Prefer stable statements that are used across at least two specs, skills, components, or docs.
- Clarify with the Developer before adding a new project-wide concept, authority rule, or evaluation output.

### Updating Statements

- Prioritize stability; do not rename established concepts without an explicit Developer direction or formal specification.
- Refine statements when usage evolves, ambiguity appears, or a project invariant needs tightening.
- Keep this file ideally under 300 lines and absolutely under 500 lines; consolidate or remove stale statements when it approaches the ideal limit.

### Agent Duty

- When an Agent encounters ambiguous or conflicting project meaning, consult `WORLDVIEW.md`. The AIDE Operating Rules in `RULES.md` codify this duty under `Context Discipline`.
- If a new concept emerges during spec, implementation, or closeout work, clarify with the Developer and propose a `WORLDVIEW.md` update before treating the concept as established.
- When citing the platform/runtime environment in worldview prose, use the exact term `AI Harness`. Do not lowercase it to `harness`.
