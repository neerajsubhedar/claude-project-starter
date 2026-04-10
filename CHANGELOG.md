# Changelog

## Unreleased

## v1.0.0 — 2026-04-09
### Added
- `init.sh` — interactive project config generator (project name, target path, stack multiselect)
- `base/CLAUDE.md` — universal rules: git branching, code style, planning, security, communication
- `base/.claudeignore` — conservative base with aggressive opt-in section
- Stack modules: `python-fastapi`, `react-vite`, `node-express`, `go`
- `ops/` placeholder directory for operational docs (latency analysis, runbooks, etc.)

### Lessons that drove this
- `2026-04-09` — axios supply chain incident: added native fetch rule to react-vite and node-express stacks
- `2026-04-09` — jq not available on all machines: prefer Python for shell scripts in this toolchain
- `2026-04-09` — working directly on master caused a PR-less merge: git branching rule added to base
