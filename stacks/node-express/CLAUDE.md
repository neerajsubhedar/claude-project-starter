## Node / Express rules
- Use async/await throughout — no callback-style error handling
- Centralized error handler middleware — never swallow errors silently
- Validate all request input at route level (zod or joi) — never trust req.body directly
- Use `node:` prefix for built-in modules (`node:fs`, `node:path`)
- Native fetch for HTTP calls (Node 18+) — not axios or node-fetch
- Pin exact versions in package.json — no `^` or `~` ranges
- Environment variables via dotenv in dev — never hardcode config values

## Project structure
- Routes in `src/routes/`
- Middleware in `src/middleware/`
- Business logic in `src/services/` — keep routes thin
- DB access in `src/db/` or `src/models/`
