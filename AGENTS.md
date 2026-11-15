# Garena R4 prototype workspace

The user is building one game feature prototype against a clock, over a laggy remote desktop, and steers in short messages.

- For a game feature prototyping task, use `$game-feature-prototype`. For setup questions or reviews, answer directly.
- Deliverable: `prototype/index.html`, self-contained, opens by double-click in Edge or Chrome. The actual task's format wins. On Windows, open it with `Start-Process .\prototype\index.html`.
- Each user message is one unit of work. Complete it, verify the part you changed, report, and end the turn. Start the next feature only when the user asks for it.
- Proceed without asking to: read workspace files, create or edit files under `prototype/`, open the prototype in a browser, research on the web, and save reference images under `prototype/`. Ask before installing packages, writing outside this workspace, or uploading or sending anything.
- `prototype/BRIEF.md` holds the session state: the task's requirement checklist, the chosen direction, assumptions, `Locked`, and `Next`. Update it when a decision changes, and keep it under 40 lines: decisions only, no verification logs (report those in the reply). After a context compaction or in a new chat, read it before editing.
- Leave everything listed under `Locked` unchanged until the user says to unlock it.
- After each verified milestone, copy `index.html` to `prototype/checkpoints/NN.html` with the next number. "回退" means restore the latest checkpoint unless the user names another one.
- `extras/` and `examples/` are reference material. Open a file there only when the user names it.
- Reply in the user's language in at most 5 short lines: what changed, where to click, what you verified, and anything you could not verify.
