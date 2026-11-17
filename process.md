# The Great Throw · process

Vibe Coding final project (Elisava MAIAD 26/27). One entry per version: what I wanted, what came out, what I decided and why.

## v1 · November 2026
**Wanted:** a circus knife-throwing game, following on from Clown License.
**Out:** first prototype (built in an earlier chat).

## v2 · 2026-11-17
**Wanted:** move from knives to flags, with world leaders as targets, the real square of each capital in the background, and a real-world data point deciding the duel.

**Decisions (and why):**
- Knives → flags: no weapons pointed at real people. Planting flags around a leader = claiming territory, encircling, applying pressure.
- Faces → faceless mannequins with sculptural hair and a matching flag: the satire comes from role and objects of power.
- Characters are named after their nation, never after a person; no words put in real politicians' mouths.
- Who starts: GDP → currency → petrol. Chosen: petrol (pump price × today's exchange rate). Readable without text, and it tells who owns the oil and who pays for it. The Brent price sets how heavy the flags are.
- No text in the game: only icons, flags, colours and numbers.
- A shared world map as the ending (from v3).

**Out:** title, country pick, pump comparison, 7-flag duel won by encirclement (6 sectors), lose if you touch the leader. Phone linked through PeerJS with a QR code. Background: YouTube live if set, otherwise a PS1-style Rome synced to real time and weather (Open-Meteo). Prices kept apart from the page in a JSON file.

## v3 · 2026-11-17
**Wanted:** a new look (references: early-2000s desktop on a CRT, PS1 low-poly characters, default user avatar with a censor bar, PS1 group cover, cracked glass with a blue screen) and the real characters.

**Decisions (and why):**
- Cast: 9 nations on equal footing, no boss. Hungary out (its government changed); the European Union replaced by France, Germany and Spain; North Korea added. Spain: current government, to be checked after the 29 November election.
- Progression: the first rival is picked freely; every win makes two linked countries "react" (REACTIONS table).
- Characters generated with Higgsfield in two sheets (Europe, powers). Chibi proportions of the powers sheet kept; Europe regenerated using it as reference.
- Skin unified in post-production to a single mannequin beige: the satire targets power, not ethnic features.
- Target: a white-and-red circus wheel that spins with the leader strapped on; flags spin with it. Collision uses the sprite's real silhouette with a 2-pixel margin.
- Losing: the glass cracks and the screen goes blue (only numbers and blocks, no text).

**Out:** CRT desktop with nation icons (conquered = your flag, reacting = blinking), taskbar clock showing the rival capital's real time, group photo for picking, pumps (North Korea censored), duel window with the wheel, ending with your flag everywhere.

## v4 · 2026-11-17
**Wanted:** a song in the game, inside an early-2000s media player.

**Decisions (and why):** the song is not uploaded as a file to the public repository (that would mean redistributing a protected track). It is played from the official video on YouTube through the embedded player. Original player design, no logos. It starts on the first click (browsers block autoplay). On a crash the music cuts out, like a frozen computer.

## v5 · 2026-11-17
**Wanted:** everything in English; the media player docked in the taskbar, like the old Windows toolbar mode; the project on GitHub.

**Decisions (and why):**
- Code, file names, data and documentation translated to English. The game itself still has no text.
- Player docked in the taskbar (play/pause, stop, visualiser, volume). The video sits in a small pop-up above it, because YouTube's rules require the player to stay visible (at least 200×200 px) while it plays: minimising it pauses the music.

**Known limits:** live cams still to be set per capital (`NATIONS[...].live`); fallback background is a generic city with real time and weather; open-arms "target" pose only for Italy and the USA; face tracking for player 2 still to do; the visualiser is animated, not driven by the real audio; versions v2–v4 in `versions/` use the old Italian file names, so their images do not load any more.

**Messages used:** to fill in.

## Dependency map
| Service | What for | Owned by |
| --- | --- | --- |
| GitHub Pages | hosting | Microsoft |
| YouTube (IFrame API, embeds) | soundtrack, live cams of the squares | Google |
| PeerJS (public server) | phone ↔ laptop link | open-source project |
| qrcode-generator (jsDelivr) | QR code for the phone | open source / jsDelivr |
| open.er-api.com | daily exchange rates | ExchangeRate-API |
| Open-Meteo | real weather of each capital | Open-Meteo (open data) |
| Higgsfield | character generation | Higgsfield AI |
| Claude | design and code, in dialogue | Anthropic |
