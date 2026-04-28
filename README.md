[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=flat-square)](https://example.com)
[![Tests](https://img.shields.io/badge/tests-pytest-blue?style=flat-square)](https://example.com)
[![Python](https://img.shields.io/badge/python-3.13+-blueviolet?style=flat-square)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-black?style=flat-square)](LICENSE)

```plaintext
			.-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-.
			|  ███╗   ███╗ ██████╗  ██████╗  ██████╗ ██████╗  ██████╗  |
			|  ████╗ ████║██╔═══██╗██╔═══██╗██╔═══██╗██╔══██╗██╔═══██╗ |
			|  ██╔████╔██║██║   ██║██║   ██║██║   ██║██████╔╝██║   ██║ |
			|  ██║╚██╔╝██║██║   ██║██║   ██║██║   ██║██╔══██╗██║   ██║ |
			|  ██║ ╚═╝ ██║╚██████╔╝╚██████╔╝╚██████╔╝██║  ██║╚██████╔╝ |
			|  ╚═╝     ╚═╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚═╝  ╚═╝ ╚═════╝  |
			'-----------------------------------------------------------'
				 Soc Ops — social bingo for IRL mixers • Neon edition
```

A tiny, snappy FastAPI + HTMX app for running in-person social bingo games. This neon-slick README dresses the project in cyberpunk neon while keeping the practical developer details front-and-center.

**Features**
- Lightweight server-rendered UI with HTMX partials.
- Deterministic, test-covered game logic in `app/game_logic.py`.
- Session-based play: no accounts, ephemeral games.
- Accessibility-minded templates and small footprint for quick deploy.

**Screenshots**
- Screenshot (game screen): assets/screenshots/game_screen.png
- Screenshot (start screen): assets/screenshots/start_screen.png
- Screenshot (modal): assets/screenshots/modal.png

(Replace the placeholders above with real images in `app/static/`.)

**Quick Start**
- Install deps and sync virtualenv:
```bash
uv sync
```
- Run tests:
```bash
uv run pytest
```
- Lint:
```bash
uv run ruff check .
```
- Start dev server:
```bash
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
"$BROWSER" http://localhost:8000   # open in host browser (do not use VS Code Simple Browser)
```

**Developer Checklist**
- Run `uv sync` after editing `pyproject.toml`.
- Lint with `uv run ruff check .` (PEP8 + type hints).
- Add or update tests in `tests/`; run `uv run pytest`.
- Keep templates idempotent; prefer small, testable partials under `app/templates/components/`.
- Commit focused changes with clear PR descriptions.

**Design Tokens**
Use these tokens in CSS or templates for consistent neon styling:
- Colors:
	- --neon-pink: #ff2d95
	- --neon-cyan: #00e6ff
	- --neon-yellow: #ffd800
	- --bg-deep: #0b0f17
- Typography:
	- Font stack: "Inter", system-ui, -apple-system, "Segoe UI", sans-serif
- Spacing:
	- --gap-sm: 8px; --gap-md: 16px; --gap-lg: 24px

(These map to `app/static/css/app.css` — update there and keep tokens synced.)

**Project Layout**
- app/ — FastAPI app, templates, static assets
	- app/game_logic.py — bingo rules & helpers
	- app/game_service.py — session orchestration
	- app/main.py — FastAPI routes
	- app/templates/ — Jinja2 + HTMX partials
- tests/ — unit & API tests
- workshop/ — guided exercises & docs

**Contribution**
- Fork + PR: feature branch → open PR against `main`
- Commit: follow small, focused commits; run tests & lint locally
- Review: add changelog blurb for user-visible changes
- Style: type hints, PEP 8, Ruff (88 char limit)

**Next Steps**
- Add Dockerfile and GitHub Actions for CI.
- Add real screenshots and small demo recording in `docs/`.
- Add optional persistent storage for multi-session tournaments.

**Reference**
- Quick commands: `uv sync`, `uv run pytest`, `uv run ruff check .`
- Dev server: `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`
- Workshop guide: `workshop/GUIDE.md`

**License**
This project is licensed under the terms in `LICENSE`. Use, modify and share with neon discretion.

---

Made with neon, caffeine, and unit tests. Keep the lights low and the logs bright.
