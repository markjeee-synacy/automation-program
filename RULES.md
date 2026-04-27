# Project Rules

## Project-Specific Rules

### Program-of-Record Artifacts
- `program-files/Mission.md`, `program-files/programs/<sub-program>/*.md`, and `program-files/<internal-program>/*.md` are program-of-record. Treat edits as program-meaning changes, not docs cleanup. Confirm with the developer before renaming, restructuring, or deleting.
- Initiative Documents under `program-files/programs/<sub-program>/initiatives/` and `program-files/<internal-program>/initiatives/` are program-of-record. Same rule applies.
- Roadmap Documents under `program-files/roadmap/<year>/`, Strategy Documents under `program-files/strategy/`, and work-system documents under `program-files/work-system/` are program-of-record. Same rule applies.
- Adding a new Sub-Program directory under `program-files/programs/` is a worldview-affecting change. Confirm with the developer and update `WORLDVIEW.md` (Sub-Program terminology + ontology) in the same change.
- Adding a new top-level directory under `program-files/` (e.g., a new content surface alongside `roadmap/`, `work-system/`, `strategy/`, `analysis/`) is a worldview-affecting change. Confirm with the developer and update `AGENTS.md` (project structure + key files) and `WORLDVIEW.md` (terminology + ontology) in the same change.

### Publishing and Co-Editing
- The Atlassian MCP writes to live Confluence pages and JIRA issues. Treat any `mcp__claude_ai_Atlassian__*` write tool (create/edit/comment/transition) as an external-facing action — confirm with the developer before invoking.
- The Google Drive MCP can read and write Google Docs that are co-edited with `program-files/`. Treat any `mcp__claude_ai_Google_Drive__*` write tool as an external-facing action — confirm with the developer before invoking.
- `program-files/` is the source of truth for what is published to Astro and Confluence and synced with Google Docs. Never reconcile a Confluence, Astro, or Google Docs copy back to `program-files/` without explicit developer direction.
- A `Wiki-link:` frontmatter field on a `program-files/` Markdown file points to the corresponding Confluence page. When pushing a file to Confluence, strip the YAML frontmatter and the redundant H1 (Confluence renders the page title separately) before sending the body.

### Program-Files Edits
- Bulk renames or deletions under `program-files/` may break the Publishing Pipeline (Astro routes, Confluence pages, Google Docs sync mappings). Confirm with the developer before bulk operations.

### Knowledge Base Edits
- Edits to `docs/kb/` are internal-only and have no publishing side-effects. Bulk renames or deletions still warrant developer confirmation because internal cross-references and AGENTS.md/WORLDVIEW.md citations may break.

<!-- AIDE:RULES:START -->
## AIDE Operating Rules

### Human-in-the-Loop
- Don't assume. Don't hide confusion. Surface tradeoffs.
- State assumptions explicitly. If something is unclear, stop, name what's confusing, and ask.
- Confirm with the developer before destructive, irreversible, or external-facing actions.
- Confirm before structural changes or dependency additions.
- When intent is ambiguous, confirm before acting.

### Execution
- Simplicity first — minimum code that solves the problem. Nothing speculative.
- Surgical changes — touch only what you must. Clean up only your own mess.
- Match existing style. Do not improve adjacent code, comments, or formatting unless the task requires it.
- Find root causes — no temporary fixes, no workarounds.
- Safety and security by design — consider from the start.
- Least privilege — only access files and tools needed for the task.
- New dependency — ask developer before introducing.
- Research the codebase before editing. Never change code you haven't read.

### Delegation
- Main session first — create subagents only when isolated context, restricted permissions, or a different model is needed.
- Single-level delegation only — subagents do not spawn subagents.
- One focused task per subagent.

### Verification
- Define success criteria. Loop until verified.
- Never mark a task complete without verifying the result.
- Prefer rules-based verification (tests, linting) over LLM-as-judge.

### Error Recovery
- Three attempts, then escalate to the developer.
- Escalate, do not guess — a wrong guess costs more than admitting uncertainty.
- Resume from checkpoint, not restart.

### Context Discipline
- One session, one focus — do not mix unrelated tasks.
- Write to files, not context — save research and plans to files.
- Load on demand — pull only what the current step requires.
- Consult `WORLDVIEW.md` when project meaning is ambiguous or contested. Do not rely on inferred meaning when a worldview surface is available.

### Values
- Grow human potential — augment the developer, surface decisions rather than deciding silently.
- Accessible and transparent — state what you are doing and why.
- Safety first, secure by design.
- Agile execution — small, focused, iteratively improved.
<!-- AIDE:RULES:END -->
