# QA checklist (run before demo, and after each milestone)

## Opens and runs
- [ ] `prototype/index.html` opens by double-click (file://), no server needed
- [ ] No errors in the browser console (F12 → Console)
- [ ] Reset (Demo Controls) returns to a clean first-time state; refresh keeps progress

## Every must-have works end to end
- [ ] Interaction 1: click path works from start to finish
- [ ] Interaction 2
- [ ] Interaction 3
- [ ] Wow moment triggers reliably (has a Demo Control shortcut)
- [ ] No dead buttons: every button gives visible feedback

## Looks like a game
- [ ] Theme tokens fit the game; one clear primary action per screen
- [ ] Realistic fake data (names, weapons, maps, numbers); no placeholder text
- [ ] Locked / empty / completed states exist where relevant
- [ ] Works at 390px wide and on desktop (phone frame centred)

## Explains itself
- [ ] Design Notes drawer: problem, target players, how it works, KPIs (primary + guardrail), risks, AI design (if any)
- [ ] Labels simulated data and simulated AI honestly
- [ ] BRIEF.md and DEMO.md exist and match what was built

## Safety net
- [ ] Latest checkpoint saved (`prototype/checkpoint-N.html`)
- [ ] If time is short: cut scope, never leave a broken screen in the demo path
