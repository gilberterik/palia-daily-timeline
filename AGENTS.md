# Repository Guidelines

## Project Structure & Module Organization
- Single‑file app: `ring_clock_app.html` at repo root.
- If you modularize:
  - `src/` for HTML partials, JS modules, CSS.
  - `assets/` for images/fonts (keep files optimized and local).
  - `tests/` for future automation (Playwright/Jest).

## Build, Test, and Development Commands
- Open in a browser: `ring_clock_app.html` (double‑click or drag into a tab).
- Local server (avoids file:// restrictions): `python -m http.server 8000` then visit `http://localhost:8000/ring_clock_app.html`.
- Optional formatting: `npx prettier --write ring_clock_app.html` (if Node is installed).

## Coding Style & Naming Conventions
- Indentation: 2 spaces; no tabs. Keep lines ~100 chars.
- HTML: use semantic tags; attributes lower‑case; classes `kebab-case`; ids sparingly.
- CSS: variables `--kebab-case`; classes `kebab-case`; prefer the `<style>` block (avoid inline style attributes). Group related rules.
- JS (if added): ES modules, `const`/`let`, camelCase for variables/functions, PascalCase only for component‑like factories. Avoid global leakage.
- Keep the file self‑contained; when splitting, prefer small focused modules with clear names.

## Testing Guidelines
- Current state: no automated tests.
- Manual checklist (per change):
  - Renders clock and updates correctly.
  - Responsive at common viewports (mobile/desktop).
  - No console errors/warnings.
  - Works in latest Chrome and Firefox.
- If adding tests, prefer Playwright for smoke/visual checks and a basic CI run.

## Commit & Pull Request Guidelines
- Use Conventional Commits: `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`, `chore:`.
- One topic per PR; keep diffs focused.
- PR description: what/why, screenshots or GIFs for UI changes, manual test notes, and linked issue (if any).

## Security & Configuration Tips
- Keep the app offline‑friendly; avoid external network calls.
- Do not commit secrets. Use local assets and verify licenses.
- Large assets: compress and document source.

