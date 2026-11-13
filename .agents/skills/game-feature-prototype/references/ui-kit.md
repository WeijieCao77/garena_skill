# UI kit for game feature prototypes

Goal: it should look like a screen from a real mobile shooter / MOBA, not a SaaS dashboard.

## Layout
- **Phone frame first**: the scaffold renders a 390×844 phone frame centred on desktop, with the Design Notes and Demo Controls drawers outside/over it. On screens narrower than 500px the frame becomes full-screen.
- Top **resource bar** (avatar, level, currencies), main content, bottom **tab bar** (3–5 tabs). Modals and reward popups overlay the frame.
- One primary action per screen, visually dominant (large, bright, bottom-reachable).

## Theme tokens (edit `:root` in the scaffold)
Pick one preset and adjust; keep contrast high on dark backgrounds.
| Preset | --bg | --panel | --accent | --accent-2 | Mood |
|---|---|---|---|---|---|
| Free Fire | #14100c | #231b14 | #ffb21a (gold) | #ff5a1f (orange) | warm, energetic, collab-heavy |
| CODM | #0d1014 | #171c22 | #f2c230 (tactical yellow) | #5fd38d (HUD green) | military, sharp, HUD lines |
| Arena of Valor | #0c1022 | #161c38 | #6ea8ff (arcane blue) | #ffd36e (gold) | fantasy, ornate |
| Esports | #0b0b12 | #15151f | #ff4655 (red) | #20e3c2 (cyan) | broadcast, bold numbers |
Rarity colours: common #9aa4b2, rare #4aa3ff, epic #b06cff, legendary #ffb21a, mythic #ff4d6d.

## Typography
- System font stack (works offline): `"PingFang SC","Microsoft YaHei","Segoe UI",system-ui,sans-serif`.
- Numbers big and bold (rewards, timers, ranks); labels small and muted. Use `font-variant-numeric: tabular-nums` for counters.
- Uppercase letter-spaced micro labels for HUD feel (e.g. `SEASON 10 · DAY 3`).

## Components in the scaffold (reuse, don't reinvent)
`.card`, `.btn` / `.btn.primary` / `.btn.ghost`, `.pill` (rarity tags), `.bar` progress bars, `.grid` reward grids, `toast(msg)`, `openModal(html)`, `rewardPopup(items)`, `aiChat` panel with typing indicator, tab router (`go('tab')`), `state` + `save()` + `render()`, Demo Controls (`demo.addControl(label, fn)`), Design Notes drawer.

## Game feel checklist (every interaction)
- Press feedback: scale 0.97 on `:active`.
- Rewards: popup with item cards + short burst animation + number count-up.
- Progress: animated bar fill; show "x/y" and what's unlocked next.
- Time pressure: countdowns (`02:13:45`) and "NEW" badges, used sparingly.
- Locked states: dimmed + lock icon + unlock condition text.
- Empty states: friendly line + one action.

## Images and icons
- Prefer inline SVG or emoji-free icon glyphs drawn with CSS; emoji only as small accents.
- Web images (weapon art, character art) are allowed as decoration with `onerror` fallback to a gradient tile. Never depend on them for layout.

## Avoid (looks generic / AI-made)
- Purple-to-blue SaaS gradients on everything, glassmorphism everywhere, centred hero + three feature cards.
- Lorem ipsum, "Feature 1/2/3", placeholder names like "Player123" (use believable gamer tags: `Zyn.Alpha`, `BOOYAH_Kai`, `ManilaSniper`).
- Too many colours; more than one primary button per screen; tiny unreadable text.
- Fake precision without labels (say "模拟数据" in the Design Notes).

## Copy
- Short, active, game-like: "领取", "前往", "再来一局", "今日剩余 2 次".
- Show the benefit, not the mechanism: "连败也不掉星" instead of "loss protection algorithm enabled".
