# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is a **GitHub profile repository** (`romoreiira/romoreiira`). Its sole purpose is to render the `README.md` as the public GitHub profile page for the user `romoreiira`. There is no application code, build system, or test suite.

## Repository structure

- `README.md` — the profile page content, written in Portuguese (Brazilian). It presents Rodrigo Moreira as an automation/AI consultant. Editing this file directly changes what visitors see at github.com/romoreiira.
- `.github/workflows/snake.yml` — GitHub Actions workflow that generates a contribution-graph snake animation SVG twice daily (every 12 hours) and on every push to `main`. It publishes the output SVGs to the `output` branch under `dist/`.

## Snake animation

The snake SVGs are referenced in `README.md` as:
```
https://raw.githubusercontent.com/romoreiira/romoreiira/output/github-contribution-grid-snake.svg
https://raw.githubusercontent.com/romoreiira/romoreiira/output/github-contribution-grid-snake-dark.svg
```

These files live on the `output` branch (not `main`) and are managed entirely by the workflow — do not edit them manually. To regenerate immediately, trigger the `Generate Snake Animation` workflow manually via `workflow_dispatch`.

## README conventions

- Language: Portuguese (pt-BR) throughout.
- Badges use `shields.io` with `style=for-the-badge`.
- Contact links (LinkedIn, WhatsApp, e-mail) must stay consistent with the actual contact details embedded in the file.
- The profile photo / avatar animation block at the bottom uses a `<picture>` element with `prefers-color-scheme` for light/dark variants — keep both `srcset` entries in sync.
