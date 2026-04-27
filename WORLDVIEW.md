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
- **KPI:** A defined performance measure (cost savings, efficiency gains, error reduction) used to track the impact of an initiative.
- **Knowledge Base (KB):** The Markdown content under `docs/kb/` that records program context, decisions, and reference material. Selected KB content is published to the Astro site, Confluence, and JIRA.

### Ontology

- **Class: Program** — The Automation Program itself. The project owns exactly one.
- **Class: Function** — A Program Function (one of the five). Belongs to the Program.
- **Class: Opportunity** — Belongs to a Function (typically Opportunity Identification & Development).
- **Class: Initiative** — Derived from an approved Opportunity. Owned by Initiative Management & Cross-Functional Execution.
- **Class: KPI** — Attached to an Initiative; rolls up to Performance Tracking & Continuous Improvement.
- **Class: Roadmap Item** — Owned by Strategy & Roadmap Development; sequences Initiatives over time.
- **Class: KB Page** — Markdown artifact under `docs/kb/`. May describe any of the above classes.
- Program → produces → Roadmap (via Strategy & Roadmap Development).
- Function → discovers → Opportunity → becomes → Initiative → measured by → KPI.
- KB Page → records → any class above.

### Axioms

- The Automation Program serves RISE's Technology department; it is not a customer-facing program.
- Initiatives are derived from approved Opportunities — an Initiative without a corresponding Opportunity is incomplete.
- Every Initiative has at least one KPI; performance claims without a defined KPI are unsupported.
- The Roadmap reflects the current Maturity Assessment plus the target vision; changes to either propagate to the Roadmap.
- Governance, Standards & Reusability constrains all other Functions — reusable frameworks and standards take precedence over one-off solutions.
- The Knowledge Base is the system of record for program meaning; downstream publishing (Astro, Confluence, JIRA) reflects the KB, not the other way around.

### Epistemology

- A claim about a Program Function is supported when it cites `docs/kb/About Automation Program.md` or a successor KB page that defines the function.
- A claim about an Opportunity or Initiative is supported only when a KB page or workflow artifact records it; otherwise the claim is `missing`.
- A KPI value is supported only when its definition and measurement source are both recorded; a number without a defined measurement is `unknown`.
- Conflicts between KB content and downstream published copies (Astro, Confluence, JIRA) resolve in favor of the KB until the conflict is reconciled explicitly.
- Absence of a KB page about a topic is `missing`, not `false` — the program may simply not have addressed it yet.

### Evaluation Outputs

- **supported:** A KB page or workflow artifact records the claim and its derivation.
- **missing:** No KB page or workflow artifact records the claim yet.
- **unknown:** Artifacts exist but cannot be interpreted confidently (e.g., a KPI number with no measurement definition).
- **conflicted:** KB content and a downstream published copy disagree and the source of truth has not yet been reconciled.

## Automation Program Platform Development

### Domain Boundary

- **Purpose:** Covers the meaning of the platform that hosts the Automation Program — the repository itself, its AIDE-based AI Harness configuration, the knowledge base directory, architecture docs, and design patterns that together make the program operable by Developers and Agents.
- **In scope:** AIDE components (agents, skills, plugins, hooks, output styles), project entry files (`AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, `CLAUDE.md`, `GEMINI.md`), platform documentation (`docs/architecture/`, `docs/patterns/`), the knowledge base directory (`docs/kb/`) as a hosted content surface, and the publishing pipelines that move KB content to Astro, Confluence, and JIRA.
- **Out of scope:** Program semantics of KB content (Opportunities, Initiatives, KPIs) — those belong to the Automation Program domain. RISE's customer-facing products are also out of scope.

### Terminology

- **Platform:** The `automation-program` repository plus its AIDE configuration, treated as a single deployable unit that serves the Automation Program.
- **AIDE:** The AI-assisted Development Environment framework that organizes the Platform's Agent-facing configuration into typed components, with shared canonical sources under `.agents/` and platform-specific entry points under `.claude/`, `.gemini/`, `.github/agents/`, and `.codex/agents/`.
- **AIDE Component:** An agent, skill, plugin, hook, or output style installed into the Platform.
- **Canonical Skill:** A skill stored under `.agents/skills/` that is shared across AI Harness platforms via symlinks or platform-specific references.
- **Project Entry File:** One of `AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, or the platform wrappers `CLAUDE.md` and `GEMINI.md` that bootstrap an AI Harness session.
- **Architecture Doc:** A Markdown file under `docs/architecture/` that records Platform structure, integration points, or deployment topology.
- **Design Pattern:** A reusable solution recorded under `docs/patterns/` describing how a recurring Platform problem should be solved.
- **Publishing Pipeline:** Content management scripts that transform KB pages into the Astro site, Confluence pages, and JIRA tickets.

### Ontology

- **Class: Platform** — The repository as a whole. Exactly one per project.
- **Class: AIDE Component** — An agent, skill, plugin, hook, or output style. Belongs to the Platform.
- **Class: Project Entry File** — A bootstrap Markdown file (`AGENTS.md`, `WORLDVIEW.md`, `RULES.md`, `CLAUDE.md`, `GEMINI.md`).
- **Class: Architecture Doc** — Markdown artifact under `docs/architecture/`.
- **Class: Design Pattern** — Markdown artifact under `docs/patterns/`.
- **Class: KB Directory** — `docs/kb/`, a hosted content surface; its pages are KB Pages in the Automation Program domain.
- **Class: Publishing Pipeline** — Scripted transform from KB Page to Astro, Confluence, and JIRA targets.
- Platform → contains → AIDE Components, Project Entry Files, Architecture Docs, Design Patterns, KB Directory.
- Project Entry File → loads → AIDE Components into an AI Harness session.
- Architecture Doc → describes → Platform structure; Design Pattern → constrains → AIDE Component implementation.
- Publishing Pipeline → reads → KB Directory → writes → Astro, Confluence, JIRA.

### Axioms

- The Platform serves the Automation Program; Platform changes that do not advance program operability are out of scope.
- Canonical Skills under `.agents/skills/` are the source of truth; platform-specific skill directories are references, not forks.
- `AGENTS.md` is the vendor-neutral entry point; `CLAUDE.md` and `GEMINI.md` are thin wrappers that import it.
- Architecture Docs describe the Platform; they do not encode program semantics or operating rules — those live in `WORLDVIEW.md` and `RULES.md` respectively.
- Design Patterns express reusable structure; a one-off implementation that diverges from a recorded Pattern requires explicit justification.
- The Publishing Pipeline is one-way: KB → external surfaces. External edits are not pulled back without an explicit reconciliation step.

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
