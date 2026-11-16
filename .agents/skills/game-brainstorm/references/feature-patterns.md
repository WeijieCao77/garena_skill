# Garena facts and brief types

Facts as of mid-November 2026, from Sea's Q3 2026 results and news coverage. Search the web for anything newer before quoting numbers in a demo.

## Garena

- Publisher and operator of online games outside mainland China. Q3 2026: 671.7M quarterly active users, 68.6M paying users (10.2%), bookings US$890M (+5.9% year on year). Free Fire drove the growth; Arena of Valor had its 10th anniversary.

## Free Fire

- Mobile battle royale: about 10-minute matches, up to 50 players, runs on low-end Android. Free Fire MAX is the higher-fidelity version.
- More than 100M daily active users in 2026. Strongest in Southeast Asia, Latin America (Brazil, Mexico) and South Asia.
- Grows through big IP collaborations, local events and creators. Free Fire × NARUTO SHIPPUDEN (2026) had a two-day tournament in Bangkok with about 5,000 visitors, 247M+ video views and 3B+ TikTok views of fan content. It won Pocket Gamer's "Best Use of IP" award. Free Fire turns 10 in 2027.
- India: banned in 2022. A standalone Free Fire India launched on 2026-10-28, with Indian servers, a Diwali event, parental consent for under-18s, daily playtime limits (3 hours for minors) and spending caps.
- Known risks: pay-to-win perception, and fatigue from very frequent live updates.

## FFWS (Free Fire World Series)

- Global Finals 2026: Bangkok, 6–28 November. 24 teams; Grand Finals on 28 November at BITEC LIVE, 12 teams, about US$1.2M prize pool.
- Viewers (reported, from Esports Charts-based coverage): the 2025 final in Jakarta peaked at about 775K concurrent; FFWS SEA Spring 2026 set a regional record of 455K+; Free Fire at the Esports World Cup 2026 about 802K.
- Fans watch on YouTube and TikTok in local languages, follow local teams, and treat players and creators as stars.

## Call of Duty: Mobile (Garena region)

- Garena publishes CODM in Singapore, Malaysia and the Philippines. Multiplayer and battle royale modes, loadouts, ranked play.
- 2026 is esports-led: Garena Masters, a Manila Summer Festival (about 4,000 fans on site, ~50K peak online), a first Battle Royale Cup, and grassroots mall and barangay events (CODM Tayo).

## Arena of Valor

- 5v5 mobile MOBA, strongest in Thailand, Vietnam and Taiwan; 10th anniversary in 2026.

## Players in these markets

Young players on shared or mid-range Android phones and unstable mobile data. They play with school or work friends and follow creators and esports closely. Don't design around mainland Chinese player habits.

## Brief types

Pick the player behavior the prototype should change, then show the benefit and the trade-off in the flow. Label seeded values as simulated.

| Brief | Mechanic to consider | Edge to show | Measure (guardrail) |
| --- | --- | --- | --- |
| Onboarding | Teach a skill, use it once, show an unlock | Veteran skips; newcomer fails and retries | First meaningful action (time to first match) |
| Ranked / matchmaking | A real choice before queuing or a useful one after | Wait time, fair teams, smurfs | Ranked matches completed (queue time, imbalance) |
| Social / squads | Match by goal, language or readiness, then join | No party, party full, spam | Invite-to-play conversion (reports) |
| Returning players / events | Show the most relevant change, one catch-up goal | Missed day, expired event, fairness to actives | Return-to-first-match (perceived fairness) |
| Pass / economy | Make value and odds clear at the decision | Low balance, duplicate reward, pay-to-win | Informed completion (complaints, drop-off) |
| Esports | Turn a viewing moment into something to play | Event over, stream down, reward claimed | Watch-to-play conversion (viewing disruption) |
| Post-match AI | One tip grounded in a match stat | Missing data, uncertainty, fairness in play | Tip applied (perceived usefulness) |
