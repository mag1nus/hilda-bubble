# Repository Guidelines

## Project Structure & Module Organization
This repository is currently a minimal scaffold. The tracked repo-specific files are `CLAUDE.md` for RTK guidance, `.rtk/filters.toml` for command filtering, `tasks/` for work tracking, and `data/testdata.csv` for starter data. When code is added, keep source in `src/`, tests in `tests/` or `__tests__/`, and static assets in `assets/` or `public/`. Avoid committing generated files, caches, or local editor state.

## Build, Test, and Development Commands
No build or test scripts are defined yet. Use RTK-prefixed commands because this repo expects compact output, for example `rtk git status`, `rtk git diff`, or, once tooling exists, `rtk npm test`, `rtk cargo test`, and `rtk npm run dev`. Prefer the smallest command that proves the change works.

## Coding Style & Naming Conventions
No formatter or linter is configured yet. Follow the language and framework defaults you introduce, and match nearby code if you are editing an existing file. Use clear, descriptive names; keep identifiers consistent within a file; and prefer ASCII unless the file already uses other characters. If you add tooling, document it in the repo and make it the source of truth.

## Testing Guidelines
Add tests alongside the code they cover and name them after the unit under test, such as `user-service.test.ts` or `test_user_service.rs`. For now, there is no coverage threshold. When adding functionality, include at least one test that demonstrates the primary behavior and run the narrowest relevant test command.

## Commit & Pull Request Guidelines
The history currently contains a single commit (`first commit`), so no commit convention is established yet. Use short, imperative messages such as `add task scaffold` or `fix parser edge case`. Pull requests should explain the change, list verification steps, and include screenshots for UI work or other visual changes.

## Agent Instructions
Read `CLAUDE.md` before making changes. Keep `tasks/todo.md` updated while working, and add any useful follow-up lessons to `tasks/lessons.md` after corrections or recurring patterns.

## Target Deliverable
This project produces a standalone HTML file with a data tab and an R circlepackeR-style graph, styled from Region Norrbotten's identity. The graph hierarchy is `cluster -> competence -> names`, with dynamic circles, click-to-zoom, PNG export, and traffic-light coloring: `<2` red, `2` orange, `>2` green. Cluster `0` renders as zoomable free competence circles without a parent cluster. Use `data/testdata.csv` as semicolon-separated starter data; rows have `competence`, `name`, and `cluster` fields. Keep it portable and backend-free.
