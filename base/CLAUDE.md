## Git branching
- NEVER commit directly to master/main
- Branch naming:
  - `feature/<short-description>` — new functionality
  - `patch/<short-description>`   — bug fixes
  - `perf/<short-description>`    — performance improvements
- Create the branch BEFORE writing any code
- Open a PR when done, ask the user to review before merging

## Code style
- No speculative abstractions — build for what's needed now
- No error handling for scenarios that can't happen
- No docstrings, comments, or type annotations on code not being changed
- No backwards-compatibility shims for removed code — delete it clean
- No feature flags or migration shims when you can just change the code
- Three similar lines of code is better than a premature abstraction

## Planning
- For any multi-file or multi-step change: confirm approach before writing code
- Use /plan for large builds to avoid wrong-direction tool calls
- One phase at a time — do not start the next phase until the current one is verified working

## Security
- Never commit .env, credentials, or secrets
- No eval, no dynamic SQL string building, no unsanitized user input in shell commands
- Validate at system boundaries only (user input, external APIs) — trust internal code
- No axios or packages with known supply chain risk — prefer native fetch / httpx

## Communication style
- Concise — no trailing summaries of what was just done
- No emojis unless asked
- Reference file:line when pointing to specific code
- Ask before taking destructive or irreversible actions (force push, drop table, delete branch)
