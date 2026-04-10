# claude-project-starter

Generates `.claudeignore` and `CLAUDE.md` for new projects. Composable base + stack modules.

## Usage

```bash
git clone https://github.com/neerajsubhedar/claude-project-starter
cd claude-project-starter
./init.sh
```

The script will ask for:
1. **Project name**
2. **Target directory** (defaults to current directory)
3. **Stacks** — select one or more: `python-fastapi`, `react-vite`, `node-express`, `go`

Output:
- `CLAUDE.md` — base rules + selected stack rules, with a `## Project` section to fill in
- `.claudeignore` — base ignores + stack-specific ignores, with aggressive opt-ins commented out
- `ops/` — directory for operational docs (latency analysis, runbooks, incident notes)

## Structure

```
claude-project-starter/
├── init.sh
├── base/
│   ├── CLAUDE.md        ← universal rules (git, code style, security, comms)
│   └── .claudeignore    ← conservative base + aggressive opt-in comments
├── stacks/
│   ├── python-fastapi/
│   ├── react-vite/
│   ├── node-express/
│   └── go/
└── CHANGELOG.md
```

## Adding a new stack

1. Create `stacks/<name>/CLAUDE.md` and `stacks/<name>/.claudeignore`
2. Add the stack name to the `STACKS` array in `init.sh`
3. Update `CHANGELOG.md`

## Adding new optimizations

When you discover a new Claude Code optimization:
1. Update the relevant `base/` or `stacks/` file
2. Log it in `CHANGELOG.md` with the date and lesson that drove it
