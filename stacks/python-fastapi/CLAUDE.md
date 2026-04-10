## Python / FastAPI rules
- Use async/await throughout FastAPI — no synchronous DB calls
- All DB operations through SQLAlchemy session — never raw SQL strings
- Pydantic schemas for all request/response validation — never pass ORM models directly to responses
- Use `field_validator` and `model_validator` for cross-field validation in schemas
- All PKs are UUID — use `uuid.uuid4()`
- TIMESTAMPTZ for all timestamps — never plain TIMESTAMP
- Computed/derived fields calculated in FastAPI on insert/update — never in the frontend or DB triggers
- Type hints on all functions; docstrings on classes only

## Alembic rules
- Always run `alembic upgrade head` after schema changes
- Run a manual DB backup before any destructive migration
- Autogenerate migrations with `alembic revision --autogenerate -m "description"`
- Downgrade function must reverse the upgrade exactly

## Dependency rules
- Pin exact versions in requirements.txt — no `~=` or `>=` ranges
- Use `httpx` for HTTP calls — not `requests`
