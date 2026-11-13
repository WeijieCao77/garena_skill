# garena_skill

A Codex workspace with one skill, `game-feature-prototype`, for building an interactive single-file HTML prototype of a mobile game feature in about 3 hours (brief → skeleton → core interactions → polish → demo).

## Quick start (Windows)
1. On this page click **Code → Download ZIP**, then unzip it (for example to `Desktop\garena_skill-main`).
   - Or with git: `git clone https://github.com/WeijieCao77/garena_skill.git`
2. Open the unzipped folder in Codex:
   - Codex app: open the folder as the project.
   - Codex CLI: `cd` into the folder and run `codex`.
3. Check the skill is loaded: type `$` or `/skills` and look for `game-feature-prototype`.
4. Paste the task and say: `用 $game-feature-prototype 做这道题，先写 BRIEF。`

Codex reads skills from `.agents/skills` in the current folder, so no install step is needed.
Note: `.agents` starts with a dot and may be hidden in File Explorer (View → Show → Hidden items).

## Fallback: install as a personal skill
Copy `.agents\skills\game-feature-prototype` into `%USERPROFILE%\.agents\skills\` (or `%USERPROFILE%\.codex\skills\`) and restart Codex.

## Contents
| Path | What |
|---|---|
| `AGENTS.md` | Workspace rules for Codex (reply in Chinese, single HTML output, checkpoints) |
| `.agents/skills/game-feature-prototype/SKILL.md` | The workflow |
| `.agents/skills/game-feature-prototype/references/` | Brief template, game context and feature patterns, UI kit, QA checklist, demo script |
| `.agents/skills/game-feature-prototype/assets/scaffold.html` | Starting template: phone frame, tabs, state, rewards, simulated AI chat, design notes, demo controls |
| `.agents/skills/frontend-design/` | Anthropic's design-planning skill (Apache-2.0), used in the brief/skeleton phase; explicit-only |
| `.agents/skills/game-engine/` | GitHub's web game skill (MIT) for an optional Canvas mini-game; explicit-only |
| `extras/skills/` | 40 vetted helper skills ranked by fit (game design audits, UX copy, motion, game feel, QA), not auto-loaded; the main skill reads them at the right phase; see `extras/README.md` |
| `examples/codm-rookie-camp/` | A finished sample (CODM new-player first week) for quality reference |
| `prototype/` | Output folder |
