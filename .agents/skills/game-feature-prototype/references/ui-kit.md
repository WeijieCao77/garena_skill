# UI for a game feature prototype

Write one sentence about the game, the screen's job, and its visual character. For example, a ranked results screen should resemble a broadcast score sheet and put the next choice beside the result. A social lobby should make availability and the reason to join easy to scan. Follow the task's reference when provided. If the brief names an existing title, inspect the closest actual screen and borrow its interaction conventions, type scale and status language.

| Surface | Start with | Make visible before the first click |
| --- | --- | --- |
| Landscape lobby or match feature | Scene, roster or play area with an attached action panel | Party or match status, objective, and the primary action |
| Portrait event or progression | A route, reward track, or ordered list that follows the mechanic | Current step, reward or unlock condition, and next action |
| Social or competitive selection | A list, roster or comparison with a focused detail area | What distinguishes the options and what the action commits to |
| Operations tool | A working view with data and controls | What requires attention, what can be filtered or decided |

- Compose one dominant working area. Use alignment, size and spacing to organize the rest. Put borders, cards, badges, meters and navigation where they convey a distinct role or state. Use a system font stack and reserve strong color for the primary action and meaningful states. Keep status legible without color alone.
- Use a relevant screenshot, item, map or character asset when it helps players recognize the context or choose. Put captions and controls in HTML. Keep text readable over imagery. If the permitted browser, asset, or generation tool is unavailable, use a clear typographic layout or simple diagram for the mechanic.
- Use native controls with clear labels, visible keyboard focus and generous targets. For overlays, prefer a native dialog with a close control, Escape handling and focus return. Review zoom and mobile width so critical text and controls stay usable.
- Couple feedback to the action. A changed status or progress label should tell the player what happened and what comes next. Use one short emphasis on the highest-value transition when it helps comprehension. Honor `prefers-reduced-motion` and keep meaning available without animation.
- Review an actual render. At first glance, the player should know where they are, what state they're in, and what action to take. Cut navigation and copy that don't help those decisions.

Design references behind this guidance

- [OpenAI Frontend prompt instructions](https://developers.openai.com/api/docs/guides/frontend-prompt) and [OpenAI’s frontend design article](https://developers.openai.com/blog/designing-delightful-frontends-with-gpt-5-4) for hierarchy, context and a usable first screen.
- [Anthropic frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) for choosing a visual direction grounded in the subject.
