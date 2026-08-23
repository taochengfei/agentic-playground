# AGENTS.md

Conventions for AI agents (and humans) doing agentic software development in this repo.

## Repo shape

- This is a **monorepo of standalone web apps**, not a service.
- Each app is self-contained under `apps/<name>/`:
  - `index.html` is the entry point.
  - Prefer zero dependencies and no build step. Inline CSS/JS is fine; a small number of local JS files is fine; a `node_modules` or build pipeline needs justification in the app's README.
  - An app may ship a short `README.md` when it has options, controls, or non-obvious details.
- Shared code between apps is the exception: if two apps want the same utility, extract it to `shared/` and document why.

## Run & verify

- Apps must run from a plain static server: `python3 -m http.server 8000` from the repo root, or by opening `index.html` directly.
- After changing an app, verify it in a browser (or headless check) before committing: no console errors, renders at 1280×800 and on a mobile viewport, works with `file://` where practical.

## Code style

- Vanilla ES modules or plain script tags — no framework by default.
- One visual concept per app; keep each app under ~500 lines of JS unless it earns its size.
- Name things descriptively; leave a short comment at the top of each app describing what it does and any controls (click, keys, touch).

## Commits & branches

- Branches: `feature/<short-slug>`, `fix/<short-slug>`.
- Commit messages: imperative, ≤ 72 chars, one logical change per commit.
- Keep the default branch green: every commit should run.

## When in doubt

- Prefer the smallest change that makes the app better.
- If a change adds a dependency, a build step, or cross-app coupling, say so in the PR/commit message.
