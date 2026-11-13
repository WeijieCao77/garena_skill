# Backup skills (not loaded automatically)

These are third-party skills that were downloaded, read and audited on 2026-11-13. They are kept outside `.agents/skills/` so they do not crowd Codex's skill list or trigger by themselves.

**To use one:** ask Codex to read it by path (for example `read extras/skills/game-feel/SKILL.md and apply it to prototype/index.html`), or move the folder into `.agents/skills/` and restart Codex.

**Audit method:** every file was downloaded and checked. These folders contain only Markdown, YAML metadata, license files and (for two Meng To skills) a self-contained demo page. They include no executable scripts and no install or network commands. A scan for shell commands, package installs, key or password access, data upload and prompt-injection wording found nothing. Each folder keeps its original license.

| Skill | Source (stars at audit) | License | Use it for | Caveat |
|---|---|---|---|---|
| game-feel | gamedev-skills/awesome-gamedev-agent-skills (~8.7k) | Apache-2.0 | Juice tiers: shake, hit-stop, pops, easing per event size | Examples are Godot/Unity; take the rules, write vanilla JS |
| game-ui-ux | gamedev-skills/awesome-gamedev-agent-skills (~8.7k) | Apache-2.0 | HUD/menu layout, safe areas, screen stack, event-driven HUD | Engine-oriented examples |
| animation-systems | MengTo/Skills (~7.4k) | MIT | Easing and duration defaults, choreography, reduced motion | Product-web motion, adapt for games |
| web-animation-design | vercel-labs/open-agents (~5.9k) | MIT | Easing rules of thumb, timing, springs | |
| emil-design-eng | emilkowalski/skills (~56k) | MIT | Polish philosophy, invisible details, when to animate | Some React-oriented advice |
| animate | emilkowalski/skills (~56k) | MIT | Build one animation from scratch in the right order | |
| review-animations | emilkowalski/skills (~56k) | MIT | Strict review of motion code | |
| find-animation-opportunities | emilkowalski/skills (~56k) | MIT | Read-only list of what should animate | |
| break-ui | emilkowalski/skills (~56k) | MIT | Worst-case data stress test (long names, zero items) | |
| prototype | emilkowalski/skills (~56k) | MIT | Several design variants behind a picker | Explicit use only; costs time |
| no-ai-design-slop | MengTo/Skills (~7.4k) | MIT | Passive quality gate against generic AI design | Overlaps with frontend-design |
| design-first-ui-prompting | MengTo/Skills (~7.4k) | MIT | Turning a fuzzy idea into a tight UI spec | |
| iterate-until-verified | MengTo/Skills (~7.4k) | MIT | Execute-and-verify loop | Mentions subagents; use the loop only |
| test-playable-web-games | MengTo/Skills (~7.4k) | MIT | Gameplay QA checklist | Browser automation optional, skip it |
| build-game-audio-feedback | MengTo/Skills (~7.4k) | MIT | Action sounds, mute control, mobile audio unlock | Use Web Audio, no files |
| build-game-inventory | MengTo/Skills (~7.4k) | MIT | Item/loot/equipment data model | |
| baseline-ui | ibelick/ui-skills (~11k) | MIT | Fast spacing/hierarchy cleanup checklist | Assumes Tailwind/React; ignore stack rules |
| fixing-accessibility | ibelick/ui-skills (~11k) | MIT | Labels, focus, contrast check | |
| fixing-motion-performance | ibelick/ui-skills (~11k) | MIT | Janky animation fixes | |

## Looked at and not included
| Skill | Why not |
|---|---|
| pbakaus/impeccable (~109k) | Needs its bundled launcher and live-browser scripts to run; heavy (2.3 MB) |
| Leonxlnx/taste-skill (~115k) | Needs Node 22 + Chrome, runs shell hooks; built for marketing websites |
| nextlevelbuilder/ui-ux-pro-max (~149k) | Depends on Python scripts that may not exist on the target machine |
| anthropics web-artifacts-builder | Needs Node/pnpm bundling |
| Whaocaii/ai-game-skills (7) | Python pipeline with multiple agents; very new, low adoption |
| gamedev-skills prototype-fast | Greybox/throwaway philosophy conflicts with a polished demo |
| PixelWao / VM233 / jamescockburn47 game skills (0–2) | Too new to trust |
