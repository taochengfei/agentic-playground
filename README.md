# AgenticPlayground

A private playground for **agentic software development**: a collection of small, self-contained web apps with a focus on graphics and animation, built and iterated on with AI coding agents.

Each app lives in `apps/<name>/` and runs directly in the browser.

## Apps

| App | What it is |
|---|---|
| [`apps/flow-field`](apps/flow-field) | Canvas particle flow-field animation (vanilla JS, zero dependencies) |

## Quick start

No build step. Either open an app's `index.html` directly in a browser, or serve the whole repo:

```sh
python3 -m http.server 8000
# → http://localhost:8000/apps/flow-field/
```

## Adding a new app

1. Create `apps/<your-app>/index.html`.
2. Keep it self-contained (HTML + CSS + JS in one or a few files, no build step) unless there's a strong reason not to.
3. Add a row to the table above.

See [AGENTS.md](AGENTS.md) for the conventions AI agents (and humans) should follow when working in this repo.
