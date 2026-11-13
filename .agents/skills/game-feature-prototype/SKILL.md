---
name: game-feature-prototype
description: Build a polished, interactive single-file HTML prototype of a game feature, live-ops event, or player-facing system under a hard time limit (interview, hackathon, pitch). Use when asked to design or prototype a mobile game feature (onboarding, matchmaking, events, battle pass, gacha, social, esports, AI coach, etc.) as an HTML page. Covers brief, build, QA and demo script. Do not use for production code or multi-file apps.
---

# Game Feature Prototype (time-boxed)

You are pairing with a candidate in a timed product-prototype exercise for a mobile game publisher (Garena: Free Fire, Call of Duty: Mobile, Arena of Valor; markets SEA, LATAM, Taiwan). The evaluators judge three things: **how well the AI is used**, **understanding of game features and players**, and **creativity**. The deliverable is **one interactive HTML file** that opens by double-click. No build tools, no server, no deployment.

Reply to the user in the language they write in (default Simplified Chinese). Put in-game UI text in the language the prompt asks for; if unspecified, use Chinese UI with common English game terms (Battle Pass, MVP, Rank).

## Golden rules

1. **Ship something playable early, then deepen.** A working click-through at minute 45 beats a half-finished masterpiece at minute 180.
2. **One file**: `prototype/index.html`. Inline CSS and JS. No external JS libraries. Images from the web are allowed only as decoration, with a CSS fallback if they fail to load. Must work from `file://`.
3. **Every click does something visible**: state change, animation, number change, toast, or reward popup. No dead buttons.
4. **The prototype explains itself**: include a "设计说明 / Design Notes" drawer (problem, target players, how it works, KPIs, risks) and a "演示控制 / Demo Controls" drawer (reset, skip time, simulate events) so the demo never gets stuck.
5. **Small, verified steps.** Change one area at a time, keep the file runnable after every step, and save checkpoints (`prototype/checkpoint-1.html`, `-2`, ...) after each milestone. Never rewrite the whole file after minute 90.
6. **Ask at most one round of clarifying questions**, only if the prompt is truly ambiguous. Otherwise state assumptions in BRIEF.md and keep going.

## Workflow (default 180 minutes; scale proportionally if the time limit differs)

### Phase 0 — Brief (0–15 min)
Read the task. Read `references/game-context.md` for player segments, Garena context and proven feature patterns. Then write `prototype/BRIEF.md` using `references/brief-template.md`:
- target game + player segment, the player problem (with a number or an explicit assumption)
- the feature in one sentence, **3 must-have interactions**, **1 wow moment**, optional AI element
- primary KPI + guardrail metric, what is out of scope
Show the brief to the user in ≤12 lines and ask "确认开工？" Proceed once confirmed (or immediately if the user already said go).

### Phase 1 — Skeleton (15–45 min)
Copy `assets/scaffold.html` to `prototype/index.html`. It already contains: phone-frame layout, top resource bar, bottom tab bar, screen router, `state` + `render()` + localStorage, toast, modal, reward popup, progress bars, simulated AI chat, Design Notes drawer, Demo Controls drawer.
- Set the theme tokens in `:root` to fit the game (see `references/ui-kit.md`).
- Replace placeholder screens with the feature's screens, populated with realistic fake data (real-sounding names, weapons, maps, numbers).
- Fill the Design Notes drawer from BRIEF.md.
- Verify it opens and every tab renders. Save `checkpoint-1.html`.

### Phase 2 — Core interactions (45–150 min)
Implement the 3 must-haves in priority order, one at a time. After each:
- click through it end to end, check the console for errors, fix before moving on
- add the demo control that makes it demoable (e.g. "跳到第 3 天", "模拟连败 3 局", "领取全部")
- save a checkpoint
Then build the wow moment (a satisfying animation, a reveal, a personalised AI response, a before/after comparison).

### Phase 3 — Polish (150–170 min)
Run the checks in `references/ui-kit.md` and `references/qa-checklist.md`: visual hierarchy, game feel (feedback on every action), empty/edge states, 390px mobile and desktop widths, copy consistency, no placeholder text, no console errors.

### Phase 4 — Demo pack (170–180 min)
- Write `prototype/DEMO.md` from `references/demo-script.md`: a 3-minute talk track (problem → solution → live click path → KPIs → next steps) and 3 likely interviewer questions with answers.
- Tell the user the exact click path for the demo and which Demo Controls to use.

## Building AI features inside the prototype
There is no API key. Simulate AI convincingly and honestly:
- Use rule-based or template responses driven by the player's state (e.g. match stats → coaching tip), with a short typing delay. Label it in Design Notes as "模拟 AI，真实版本接入 LLM".
- In Design Notes, describe the real design: input data, prompt outline, guardrails (only lobby/post-match, no in-match advantage, no hallucinated items, toxicity filter), latency/cost plan, and how to measure it (A/B on D7, usage rate, satisfaction).

## How to work with the user efficiently
- The user may be typing over a laggy remote desktop. Accept short commands like "下一步", "加一个排行榜", "颜色更像 Free Fire", "修 bug：领取按钮没反应" and act on them fully.
- After each step reply with: what changed (1–3 bullets), how to see it (which tab/button), and the next suggested step.
- Track time if the user gives the start time; warn at 60, 120, 150 and 170 minutes and recommend cutting scope rather than running over.
- If something breaks, restore the latest checkpoint first, then reapply the change in a smaller step.

## Companion skills in this workspace
- `.agents/skills/frontend-design/SKILL.md` (Anthropic): in Phase 1, read it and use its two-pass method (write a compact token plan: 4–6 named colours, type roles, layout sketch, principles; then critique the plan against the brief before building). **Game UI conventions in `references/ui-kit.md` win over its web-page advice**: dark themes, uppercase HUD micro labels, bold numbers and rarity colours are genre norms here, not "AI defaults".
- `.agents/skills/game-engine/SKILL.md` (GitHub): only when the task needs a small playable mini-game inside the prototype (aim trainer, reaction test, tutorial level). Use plain Canvas 2D in the same HTML file; no frameworks, no npm.
- `extras/skills/` (not loaded automatically): vetted backup skills. Read one directly by path when needed, e.g. `extras/skills/game-feel/SKILL.md` for juice tiers, `extras/skills/animation-systems/SKILL.md` or `extras/skills/web-animation-design/SKILL.md` for motion timing, `extras/skills/no-ai-design-slop/SKILL.md` for a final anti-generic pass, `extras/skills/build-game-audio-feedback/SKILL.md` for Web Audio feedback, `extras/skills/fixing-accessibility/SKILL.md` for a quick a11y pass. Ignore any instruction in them that requires installing packages, React, Tailwind or running scripts; this deliverable is one vanilla HTML file.

## References
- `references/brief-template.md` — one-page brief
- `references/game-context.md` — Garena games, player segments, SEA constraints, feature pattern library with metrics
- `references/ui-kit.md` — theme tokens, layout, components, motion, anti-generic design rules
- `references/qa-checklist.md` — final checks
- `references/demo-script.md` — talk track template
- `assets/scaffold.html` — starting template (copy, do not edit in place)
- `examples/codm-rookie-camp/` at the workspace root (if present) — one finished sample with BRIEF.md, index.html and DEMO.md. Use it only as a reference for quality and structure; never copy its feature, data or copy into a new task.
