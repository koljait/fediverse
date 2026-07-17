# fediverse

A single static web app, `index.html` — "Life OS // 10-Minute Daily Reset". It is
vanilla HTML/CSS/JS with no build step, no dependencies, and no backend. All state
is persisted client-side in browser `localStorage` under the key `life-os-v1`.

## Cursor Cloud specific instructions

- This repo has no package manager, build system, tests, or linter. There is nothing
  to install; `index.html` is the entire application.
- Run it in development by serving the folder as static files, e.g.
  `python3 -m http.server 8000` from the repo root, then open `http://localhost:8000/`.
  Any static file server works; there is no framework or hot-reload — just refresh the
  browser after editing `index.html`.
- Core functionality to smoke-test: fill in "North Star" + "Tiny Move" (both required),
  click "Save Daily Reset", and confirm the status line and the "Your Momentum" streak
  update. Streak logic is date-based (compares `lastDate` to today), so it advances at
  most once per calendar day; to re-test a fresh streak use the "Reset Streak" button or
  clear the `life-os-v1` localStorage key.
