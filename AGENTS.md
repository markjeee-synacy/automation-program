# AGENTS.md

## Project

- **Name:** RISE Automation Program
- **Description:** Centralized hub for managing the RISE Automation Program — a Markdown knowledge base and workflows platform with content management scripts. The knowledge base is published as a standalone Astro site self-hosted on AWS; selected content is also published to Confluence and JIRA via the Atlassian MCP.
- **Stack:** TypeScript, Node.js, Astro

## Project Structure

```
automation-program/
├── AGENTS.md                  # This file — vendor-neutral project instructions
├── WORLDVIEW.md               # Project worldview (meaning, ontology, axioms)
├── RULES.md                   # Project rules + AIDE Operating Rules
├── CLAUDE.md                  # Claude Code wrapper (imports @AGENTS.md)
├── GEMINI.md                  # Gemini CLI wrapper (imports @AGENTS.md)
├── README.md
├── .agents/skills/            # Shared canonical skills (multi-platform)
├── .claude/                   # Claude Code (agents/, skills→symlink)
├── .gemini/agents/            # Gemini CLI agents
├── .github/agents/            # Copilot CLI agents
├── .codex/agents/             # Codex CLI agents
├── docs/
│   ├── architecture/
│   ├── patterns/
│   └── kb/                    # Internal knowledge base content (not published)
└── program-files/             # Program-of-record; published to Astro/Confluence, co-edited via Google Docs
    ├── Mission.md
    └── programs/              # One subdirectory per Sub-Program
        ├── artificial-intelligence/
        ├── business-intelligence/
        ├── enterprise-automation/
        └── network-intelligence/
```

## Commands

<!-- No package.json or build tooling exists yet. Fill in once the Astro site
     and content management scripts are scaffolded.
     Example once tooling is in place:
     - **Build:** `npm run build`
     - **Dev server:** `npm run dev`
     - **Test:** `npm test`
     - **Lint:** `npm run lint`
-->

## Key Files

- `README.md` — Project overview and tech stack summary.
- `program-files/Mission.md` — Authoritative Automation Program mission statement.
- `program-files/programs/<sub-program>/` — One directory per Sub-Program (Artificial Intelligence, Business Intelligence, Enterprise Automation, Network Intelligence), each with its own `*.md` describing goals.
- *(To be added)* `docs/kb/` — Knowledge base pages for RISE background, program scope, and the five program functions.
- *(To be added)* Astro site entry points and configuration.
- *(To be added)* Content management scripts for KB → Astro / Confluence / JIRA publishing.

## Environment

<!-- No .env.example or runtime version files detected yet. Fill in as the
     toolchain is established.
     Example once tooling is in place:
     - **Node.js:** v20+
     - **Environment variables:** Copy `.env.example` to `.env` and fill in values
     - **Setup:** `npm install`
-->

## Code Style

<!-- Fill in as project-specific conventions are established (TypeScript style,
     Astro component conventions, Markdown frontmatter rules for KB pages). -->

## Testing

<!-- Fill in once a test setup exists. -->

## Workflow

For execution principles (planning, verification, error handling, context management), see **AIDE Operating Rules** in `RULES.md`. For AIDE architecture guidance, see **aide**. Add project-specific workflow notes below.

#### Levels of Coding Control
| Level | Code Areas | Developer Role | AI Role |
|---|---|---|---|
| **High control** | Business logic, security, auth, financial, infrastructure, customer-facing | Writes specs, reviews every change, approves before merge | Implements per spec, explains trade-offs, flags concerns |
| **Standard** | Application features, API endpoints, data models | Reviews implementation, approves spec | Plans, implements, tests, requests review |
| **Low control** | Boilerplate, config, scaffolding, tests, docs, formatting | Spot-checks, trusts AI output | Takes the lead, commits directly, developer reviews later |

## Content Placement

- **AGENTS.md** — Project context, workflow, structure. Keep stable and lean.
- **Skills (`.agents/skills/`)** — Domain knowledge, checklists, patterns, code standards. Shared across platforms.
- **Agent specs** — Platform-specific. Added only when needed beyond the main session.
- **`docs/`** — Source of truth for documentation. Reference, don't duplicate.
- **`program-files/`** — Program-of-record artifacts: the Mission and per-Sub-Program directories. Edits here change program meaning AND have publishing side-effects (Astro site, Confluence pages) and co-editing side-effects (Google Docs sync). Not a documentation surface.

## Agent Architecture

The main session has access to all instructions, skills, and MCP tools. Additional agents are optional — add only when isolated context, restricted permissions, or a different model is needed.

<!-- Agent index: Add platform-specific agent sections here when you create your first agent.
     ### Claude Code (`.claude/agents/`)
     - **Agent Name** `.claude/agents/agent-name.md` — One-line description. Model: sonnet. -->

## Gotchas

- Do NOT load unless needed: full codebase, all skills at once, all agent specs.
- Knowledge base content (`docs/kb/`) drives downstream publishing to the Astro site, Confluence, and JIRA via the Atlassian MCP. Edits to KB pages may have publishing side-effects — confirm with the developer before bulk renames or deletions.

## Additional Context

<critical_instruction>
On the very first turn of the session, you MUST immediately use your file viewing tools to read the persistent system contract in this order before answering any user queries or performing other tasks: `AGENTS.md` first (already loaded or currently visible), `WORLDVIEW.md` second, and `RULES.md` third. The order is binding by default unless the Developer gives an explicit contrary instruction.
</critical_instruction>

@WORLDVIEW.md
@RULES.md

<!-- Auto-loaded Skills: Add skills here if your project needs specific skills loaded at session start.
### Auto-loaded Skills

At session start, load the following skills **before responding to any request.** Only load if discoverable from project skill directories (`.agents/skills/`) or installed plugins — if not found, skip silently.

- **skill-name** — Description of the skill and when it activates.
-->
