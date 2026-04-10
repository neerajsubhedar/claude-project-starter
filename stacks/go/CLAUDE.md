## Go rules
- Always handle errors explicitly — never `_` an error return unless provably safe
- Return errors up the call stack — no `log.Fatal` deep in library code
- Use `errors.Is` / `errors.As` for error inspection — not string matching
- Interfaces defined at point of use (consumer), not at point of implementation
- Context as first argument on all functions that do I/O or can be cancelled
- Table-driven tests with `t.Run` subtests — not repetitive test functions
- No `init()` functions — use explicit initialization in main or constructor functions

## Project structure (standard layout)
- `cmd/<app>/main.go` — entry point
- `internal/` — private packages not importable by external modules
- `pkg/` — public reusable packages (only if genuinely reusable)
- No circular imports — keep dependency graph a DAG

## Dependency rules
- Commit `go.sum` — never `.gitignore` it
- Minimal dependencies — prefer stdlib over third-party where reasonable
