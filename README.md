# Project Graph (no-tauri) — GitHub Pages embed build

This repository redistributes **built static assets only** of [Project Graph](https://github.com/graphif/project-graph) (@graphif/project-graph), GPL-3.0-only.

## Live URL

- Site: https://wagyb.github.io/mathbox-pg-pages/
- Mathbox iframe: https://wagyb.github.io/mathbox-pg-pages/?frame=true
- Repo: https://github.com/wagyb/mathbox-pg-pages (branch `main` → Pages `/`)

## Source

- Upstream: https://github.com/graphif/project-graph
- Local vendor clone (Mathbox workspace, gitignored): `.scratch/vendor-project-graph`
- Build: `VITE_BASE=/mathbox-pg-pages/ pnpm --filter @graphif/project-graph build` (or root `build:no-tauri` with same `VITE_BASE`)

## Embed in Mathbox

1. Open Course workspace → left map (Project Graph panel).
2. Paste `https://wagyb.github.io/mathbox-pg-pages/?frame=true` into **嵌入 URL** → **应用**.
3. Optional (rebuild Mathbox): set the same in `.env.local` as `VITE_PROJECT_GRAPH_URL` (see mathbox `.env.example` comment). Do **not** overwrite an in-progress tunnel `.env.local` blindly.

Mathbox does **not** merge GPL `app/` sources into its product `src/`. iframe hosting ≠ combining works into Mathbox's MIT tree.

## Known web degradations

Official PG marks「网页端」as unsupported product surface. This Pages build is a **self-hosted experiment**:

- No Tauri desktop APIs (OS file dialogs, native FS, auto-update, etc.)
- Some desktop-only tools / backends may be missing or degraded
- Suitable for iframe course-map browsing; not a full desktop feature parity claim

## License

See LICENSE (GPL-3.0). Corresponding source: upstream repository above (same version as the vendor checkout used to produce this dist). See SOURCE.md.
