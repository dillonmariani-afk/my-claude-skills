# Upstream

- Source: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
- Version: 2.15.0
- Commit: 56ea9cf174ed86786187daa9de0e6247cb0747e4 (2026-10-15)
- License: MIT (see `LICENSE`)

## What was copied

Only `.claude/skills/ui-ux-pro-max/` (SKILL.md, references, data, scripts).
The upstream test suite (`scripts/tests/`) was left out. The other upstream skills
(ui-styling, design, design-system, brand, slides, banner-design) have not been
reviewed and are not included.

The `.claude/skills/` layout is kept on purpose: SKILL.md calls its search script at
`${CLAUDE_PLUGIN_ROOT}/.claude/skills/ui-ux-pro-max/scripts/search.py`.

## Review notes (2026-10-15)

- Scripts are Python 3 standard library only (csv, json, re, pathlib, ...).
- No network calls, no subprocess/shell execution, no environment secrets read.
- Only file writes: `--persist` writes `design-system/<project>/MASTER.md` under `--output-dir`.
- Data CSVs and references scanned for embedded instructions; none found.

## Updating

1. Clone upstream at the new tag/commit.
2. Diff `.claude/skills/ui-ux-pro-max/` against this copy and review the changes.
3. Copy over, drop `scripts/tests/`, bump versions in `plugin.json` and
   `.claude-plugin/marketplace.json`, and update this file.
