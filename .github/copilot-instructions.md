---
applyTo: "**"
---

# Project Guidelines (condensed)

## Mandatory Development Checklist
- **Lint:** `uv run ruff check .`
- **Install/Build:** `uv sync`
- **Test:** `uv run pytest`

## Code Style
- Python 3.13+, type hints, PEP 8, Ruff (line length 88)

## Architecture (summary)
- Backend: FastAPI async endpoints
- Frontend: HTMX + Jinja2
- Game logic: `app/game_logic.py`; sessions in `app/game_service.py`

## Quick Commands
- Install deps: `uv sync`
- Run tests: `uv run pytest`
- Lint: `uv run ruff check .`
- Dev server: `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`
- Open in browser: `"$BROWSER" http://localhost:8000` (do not use Simple Browser)

## Conventions
- 5x5 bingo board with center free space; winning = 5 in a row
- Use HTMX for partial updates; keep templates small and idempotent

## Notes
- Workshop project (Copilot Dev Days). See `workshop/` for guides.
- Prefer linking to docs over duplicating them; keep instructions minimal.
<parameter name="filePath">/workspaces/my-soc-ops-python/.github/copilot-instructions.md