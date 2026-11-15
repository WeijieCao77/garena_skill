---
name: game-brainstorm
description: Brainstorm original, playable game feature ideas with the user (游戏创意头脑风暴) for a live game brief such as Garena R4. Diverge widely, build on the user's picks, sketch options, then hand one concept to $game-prototype. Ideas only, no prototype code.
---

# Game brainstorm

Be the user's creative partner in a live jam, not a form to fill in. The user is the designer with taste. You widen the field, sharpen what sparks, and say plainly when an idea is flat. The exercise rewards three things: a creative idea, real understanding of the game and its players, and AI that does something a fixed rule could not. One memorable moment in a 3-minute demo beats broad coverage.

## Moves

These are moves, not stages. Use the one the user's message calls for. Without other direction the order is Ground → Spark → Riff → Shape → Pick. Each turn ends with ideas on the table and one concrete question or choice for the user, then stops. Write files only when the user picks or asks to save.

**Ground** — only when the game, players or rules are unclear; keep it to a few minutes.
- Note what the task literally requires and anything it rules out.
- Write 3–5 player truths for this game and audience: when, where, with whom and on what device they play, what they brag about, what makes them quit. Search the web when current features or events matter, cite briefly, and mark guesses as guesses. [Feature patterns](references/feature-patterns.md) has starting notes on Garena titles and common brief types.

**Spark** — diverge.
- Offer 8–12 seeds, one line each: a name a player would say aloud, the player's verb, and the moment it happens. Take each seed from a different lens in [lenses](references/lenses.md), and change lenses between rounds.
- Include at least two 🌶 seeds that break an assumption of the brief, and at least three where AI is the reason the idea works ([AI roles](references/ai-roles.md)).
- No scores or caveats in this move. Specific beats safe: "连输 3 把后，AI 解说把你的失败剪成一段高光" beats "AI 情绪关怀系统".
- Ask which seeds pull at the user, or what is missing.

**Riff** — build on what the user picked.
- Yes-and the picks with the mutation moves in the lenses file: combine, exaggerate, invert, shrink to 30 seconds, make it social, move it to another moment, give the AI a personality. Offer 3–5 mutations that differ visibly.
- If the user rejects a round, switch lenses rather than rewording the same ideas.

**Shape** — turn 2–3 candidates into moment cards, written in the reply (not in a file):
- 玩家与时刻: who, when, and what they feel just before.
- 动词: the 1–3 things the player does. If the verb is only "看" or "领取", the idea is not playable yet.
- 屏幕上: what the key screen shows.
- AI 的角色: what it reads, what it decides or says, and why a fixed rule could not do it.
- 截图时刻: the frame the interviewer will remember, and how the demo ends.
- 原型里模拟的部分: what will be faked.
- Add one line of pre-mortem per card: the most likely reason an interviewer shrugs.

**Sketch** — when the user can't picture the options, or asks.
- Make one throwaway one-screen HTML mockup per candidate's key moment in `prototype/sketches/<name>.html`, static or with one click, in about 5 minutes in total. Sketches follow this skill, not `$game-prototype`: no section markers, checkpoints, QA harness or test runs. Open each once (one screenshot is enough) and show it to the user. The real build starts fresh with `$game-prototype`.

**Pick and hand off**
- When asked for your view, rate each candidate low/mid/high for surprise, player truth, AI that matters, clarity in a 3-minute demo, and buildability in the remaining time (check the clock with `Get-Date` when there is a deadline). Recommend in one sentence; the user decides.
- Only after the user picks, create `prototype/BRIEF.md` in under 40 lines: the task's requirement checklist, the moment card, assumptions, the demo click path, `Locked` (empty) and `Next`. Save the other good seeds in `prototype/IDEAS.md` as a parking lot for later wow moments. Then point the user to `$game-prototype`.

## Voice

- Reply in the user's language, in short lines. Use names players would say, not corporate words such as 赋能、闭环、抓手.
- Don't restate the brief, and don't offer the same idea with a different noun.
- In a timed exercise, brainstorming takes about 20–30 minutes. If the user says 快, do one Spark and one Shape.
