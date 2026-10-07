# Project Graph (no-tauri) — GitHub Pages embed build

This repository redistributes **built static assets only** of [Project Graph](https://github.com/graphif/project-graph) (@graphif/project-graph), GPL-3.0-only.

## Source

- Upstream: https://github.com/graphif/project-graph
- Local vendor clone (Mathbox workspace, not committed): .scratch/vendor-project-graph
- Build: pnpm build:no-tauri / pnpm --filter @graphif/project-graph build with VITE_BASE=/mathbox-pg-pages/

## Embed URL (Mathbox iframe)

`https://<user>.github.io/mathbox-pg-pages/?frame=true`

Mathbox does **not** merge GPL pp/ sources into its product src/. iframe hosting ≠ combining works into Mathbox's MIT tree.

## License

See LICENSE (GPL-3.0). Corresponding source is the upstream repository above (same version as the vendor checkout used to produce this dist).
