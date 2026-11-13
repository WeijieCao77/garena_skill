# Game context for Garena-style feature prototypes

Use this to make the prototype feel like it belongs in a real Garena game and to justify design choices with player behaviour and metrics. Treat numbers marked "illustrative" as assumptions and say so in the brief.

## Garena portfolio (public facts)
- **Free Fire / Free Fire MAX** (self-developed, 2017): light battle royale, ~50 players, ~10-minute matches, runs on low-end phones. Strongest in SEA, LATAM (Brazil), India (MAX). Premium currency: Diamonds. Seasonal pass: Booyah Pass. Modes: Battle Royale, Clash Squad (4v4 rounds). Characters with skills, pets, gloo walls, many IP collaborations. Over 100M daily actives (2026). 10th anniversary in 2027.
- **Call of Duty: Mobile** (licensed from Activision, developed by TiMi; Garena publishes in SEA/Taiwan regions): Multiplayer (Team Deathmatch, Domination, Search & Destroy, Hardpoint), Battle Royale, Ranked, Gunsmith loadouts, Operators, Scorestreaks, Clans. Premium currency: CP. Seasonal Battle Pass. Strong esports scene in the Philippines.
- **Arena of Valor** (licensed MOBA, 5v5): strong in Taiwan, Thailand, Vietnam; 10th anniversary in 2026.
- Newer titles built on global IP (e.g. Palworld-licensed and Monster Hunter-licensed mobile games).
- Garena business in Q3 2026: bookings growth slowed (+5.9% YoY), quarterly actives flat (~672M), growth came from paying ratio (10.2%). Implication: **new and returning players are the growth lever**; monetisation must not hurt fairness.

## Player segments (pick one per prototype)
| Segment | Typical behaviour | Common pain points | Typical goals |
|---|---|---|---|
| New players (first 7 days) | Few matches, bot lobbies first, low K/D | Skill gap vs veterans, too many modes/systems, no friends, unclear next goal | D1/D7 retention, first-week matches |
| Competitive | Ranked grind, studies loadouts, watches pros | Unfair matches (cheaters, smurfs, AFK teammates), no actionable feedback, rank feels meaningless | Ranked participation, season retention |
| Social | Plays with friends/clan, joins for events | Hard to find squad, friends inactive, little to do together outside matches | Squad rate, invites, session length |
| Returning (lapsed 14–30+ days) | Comes back for events/collabs | Game changed, friends gone, feels behind | Return D7, reactivation rate |
| Payers (whales / dolphins / minnows) | Buy passes, gacha, bundles | Poor value perception, duplicates, FOMO fatigue | Paying ratio, ARPPU, without hurting fairness |
| Viewers / esports fans | Watch tournaments, follow teams | Watching and playing are disconnected | Watch-to-play conversion |

## SEA / emerging-market constraints (use as design considerations)
- Low- to mid-range Android phones, limited storage → small downloads, light effects, optional asset packs.
- Expensive or unstable mobile data → offline-tolerant flows, small images.
- Short sessions (commute, breaks) → tasks that fit in 5–10 minutes.
- Many languages (Thai, Bahasa Indonesia, Vietnamese, Tagalog, Portuguese) → short UI copy, icons.
- Fragmented payments (e-wallets, carrier billing, top-up cards) → clear price/value display.
- Strong community and creator culture (Facebook, TikTok, YouTube, local streamers) → share cards, referral codes.

## Feature pattern library
Each entry: mechanic → key design considerations → KPIs. Combine 1–2 patterns; do not stack everything.

- **Guided first week (新手 7 日成长路线)**: daily 2–3 small goals, unlock modes gradually, day-7 reward. → Keep goals completable in one session; reward should teach (e.g. a good starter loadout). → D1/D7, goal completion rate.
- **Protected matchmaking (新手保护匹配)**: first N real matches with similar newcomers; loss-streak softening; smurf detection. → Queue-time trade-off, gradual exit (ramp, not cliff), don't reveal "easy mode". → Early K/D, D7, queue time (guardrail).
- **AI coach / companion (AI 教练)**: post-match review, loadout suggestions, Q&A in local language. → Only lobby/post-match (fairness), grounded in game data, opt-in, short answers. → Usage rate, D7 lift via A/B, satisfaction.
- **Comeback / return program (回流)**: "what's new" recap, catch-up rewards, re-matched with active friends. → Don't punish loyal players; time-limited. → Reactivation rate, return D7.
- **Mentor / buddy (老带新)**: veteran mentors newbies, both earn cosmetic rewards on milestones. → Anti-abuse (same device, alt accounts), mentor quality score, report button. → Squad rate, newbie D7, mentor participation.
- **Squad finder / clan board (组队广场)**: post a squad request with mode, rank, voice, language. → Safety, filters, quick-join. → Squad rate, session length.
- **Season / Battle Pass**: free + premium track, weekly missions. → Value clarity, catch-up for late joiners. → Pass purchase rate, mission completion.
- **Gacha / lucky draw with pity (抽奖 + 保底)**: show odds, pity counter, duplicate conversion. → Transparency, spending limits, no pay-to-win stats. → Paying ratio, ARPPU, complaint rate (guardrail).
- **Collection / login calendar events**: collect tokens daily, exchange shop. → Missed-day catch-up. → DAU during event, return rate.
- **Esports watch-to-earn / prediction (观赛得奖励 / 赛事竞猜)**: watch minutes or predictions unlock in-game rewards; team-themed cosmetics. → Link to real schedule, avoid gambling framing. → Viewer-to-player conversion, event DAU.
- **Anniversary / memory recap (周年回忆)**: personal stats recap ("your first gun, total matches"), shareable card. → Privacy, nice share image. → Share rate, reactivation.
- **Fair-play & reporting feedback (举报反馈)**: tell reporters when action was taken. → Don't expose details. → Report satisfaction, ranked retention.
- **Highlight / clip sharing (高光时刻分享)**: auto-generated best moments with share. → Small file size. → Shares, installs from shares.

## Metrics glossary (use the right word)
DAU / MAU (stickiness = DAU÷MAU), D1/D7/D30 retention, session length, matches per day, conversion (paying ratio), ARPU / ARPPU / ARPDAU, LTV vs CAC, K/D, queue time, completion rate, A/B test with control group.

## Good default assumptions (illustrative, label as assumptions)
- New player D1 ~35%, D7 ~10–15% for mobile shooters.
- 50%+ of day-1 churners never finished 5 real matches.
- Returning players who rejoin with a friend retain ~2× better than solo returners.
