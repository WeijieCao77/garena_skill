# AI roles in a game feature

An AI idea is strong when it needs AI: it takes open-ended input (free text or voice), personalizes from many signals, generates new content, or judges nuance. If a lookup table would give the same result, it is a rule, not AI.

| Role | What it does for the player | Example moment |
| --- | --- | --- |
| Duo partner | Plays or talks alongside you, with a personality | A bot teammate who remembers your habits and says so |
| Coach | One suggestion grounded in a stat from your last match | "You died 6 times crossing open ground; try this route" |
| Caster or commentator | Narrates your play as if it were an esports match | A hype replay of your best round with live commentary |
| Storyteller | Turns your history into a story | A "your ten years in the game" chapter book for returning players |
| Director | Shapes the event or difficulty around you | A comeback mission tuned to what you are bad at |
| Matchmaker | Matches by vibe, language or goal, not only rank | "Chill duo for 20 minutes, Bahasa, mic on" |
| Character with memory | An NPC or pet that remembers what you did | A pet that reacts to your losing streak |
| Creator tool | Generates a spray, emote, loadout name or squad banner from text | A squad banner made from your inside joke |
| Referee or safety | Judges nuance in chat or behavior | Warns before a toxic message is sent |
| Translator | Lets mixed-language squads talk | Live subtitles in squad voice chat |
| Quest giver | Writes goals from your play style | Three personal challenges for tonight |

## Faking it convincingly in one HTML file

- Seed 2–3 contrasting player profiles and let the AI output change visibly when the profile changes.
- Build replies from templates filled with the player's data, with some variety. Show a short "thinking" state.
- Show what the AI used ("基于你最近 20 局"). Label it 模拟 AI.
- For free-text input, match keywords and fall back gracefully when nothing matches.

## Questions an interviewer may ask

What data does the real version need? How do you stop it from making things up? Is it fair in competitive play? What about privacy, minors and cost per call? Prepare one sentence for each.
