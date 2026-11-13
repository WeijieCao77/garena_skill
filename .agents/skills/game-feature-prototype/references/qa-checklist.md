# Check the delivered HTML

- Open `prototype/index.html` from Windows Explorer or run `Start-Process .\prototype\index.html` in PowerShell. Check that the URL starts with `file://`. If a browser tool is available, use it to inspect the actual render and console. Otherwise follow the same steps in Edge or Chrome and check F12 → Console.
- From the starting state, use the same visible controls a reviewer will use. Check each task requirement, the state change after the main action, and a relevant blocked or empty state. Try a rapid repeat when there is a reward, spend or submission. Ensure reset or reload gives the intended state and that pending timers cannot overwrite a reset.
- Check the first viewport at desktop presentation size and the intended game viewport. Look for clipping, unreadable text, hidden actions, focus visibility, and misleading or inactive controls. Keyboard-check the main path and any dialog. If the screen relies on media, verify the main path still works when that media cannot load.
- Replay the exact path once more after the last edit. Record what was actually observed and provide manual steps for checks you could not run.
