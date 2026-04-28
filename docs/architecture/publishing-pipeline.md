# Publishing Pipeline

How program-of-record content under `program-files/` reaches its three external surfaces — the Astro site, Confluence, and Google Docs — and how Jira fits the broader collaboration model.

## Sources of truth

- `program-files/` is the program-of-record and the source for the Publishing Pipeline. The Mission, Sub-Programs, Internal Programs, Roadmap, Strategy, and work-system documents all live here.
- `docs/kb/` is internal-only knowledge base content. It is **not** part of the Publishing Pipeline and is never read by it.

## Surfaces and direction

| Surface | Direction | Mechanism | Conflict policy |
|---|---|---|---|
| Astro site (self-hosted on AWS) | One-way: `program-files/` → site | Build step renders Markdown to static pages; deployed to AWS | `program-files/` wins; reconcile downstream only with explicit developer direction |
| Confluence (Wiki pages) | One-way: `program-files/` → Confluence | Atlassian MCP `createConfluencePage` / `updateConfluencePage`; `Wiki-link:` frontmatter on the source file points to the destination page; YAML frontmatter and the redundant H1 are stripped before sending the body | `program-files/` wins; never reconcile a Confluence copy back without explicit developer direction |
| Google Docs | Bidirectional: `program-files/` ↔ Doc | Google Drive MCP read/write of co-edited Docs | Conflicts require explicit developer direction (sync is bidirectional) |

## Jira (collaboration, not publishing)

Jira issues/cards are not part of the Publishing Pipeline. They are used via the Atlassian MCP for ticket collaboration with program participants — Work Items on Work Boards, Objective tracking on the AUTO project Jira timeline (Strategy Process), and per-program Develop boards (EA, BI, NI, etc.). Work Boards are indexed in `program-files/work-system/Work Boards.md`.

## Write-tool gates

All Atlassian MCP and Google Drive MCP write tools are external-facing. They require developer confirmation before invocation. See `RULES.md` → Publishing and Co-Editing.

## Implementation status

The repository does not yet contain Astro site code, Confluence/Google Docs sync scripts, or build/deploy configuration. The contract above describes the intended pipeline. Implementation surfaces (script entry points, configuration, CI/CD wiring) will be added under this directory as they are built; AGENTS.md will be updated to reference them at that point.

## See also

- `AGENTS.md` — MCP Tools section enumerates the read/write tool surfaces.
- `WORLDVIEW.md` — Automation Program Platform Development domain (Publishing Pipeline class and axioms).
- `RULES.md` — Publishing and Co-Editing rules; Program-Files Edits rules.
