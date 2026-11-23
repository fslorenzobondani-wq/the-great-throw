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

## v6 · 2026-11-19
**Wanted:** a game that runs on its own and is clear to an audience: the phone as controller seen by the webcam, real data that matters, scenario cards that tell real politics, a match for several players, a bigger reaction when you hit a leader, the city videos in full view.

**Decisions (and why):**
- **Soundtrack as an mp3 in the repository**, played with Web Audio: a real visualiser in the taskbar and a tape-stop when the leader is hit. The YouTube media player was ugly on screen and has been removed. Lorenzo chose to host the file knowing the repository is public.
- **Intro like an early-2000s computer** (boot, modem dial-up), then a title with the skyline. The globe was removed from the title: too many things.
- **Currency instead of petrol:** every nation's coin is measured against gold, today vs two days ago. The weaker coin gets the advantage (the wheel starts still). Same currency → coin toss. North Korea's coin is censored.
- **Phone = controller, webcam = eye:** the phone shows its flag full screen on a pink frame; the laptop webcam follows the pink to aim and detects the throw when the phone moves forward fast or flicks. Swipe and touchpad throws were tried first and did not work well enough. Backups: Space, a tap on the phone, the mouse.
- **City videos from Wikimedia Commons** (free licences) instead of live cams, which were unreliable. Local time tints them, real rain falls on them. No real faces: Riyadh has no video.
- **Match for 2–4 players with one phone passed hand to hand:** several pink phones would confuse the webcam. Everyone shares out the 9 countries in turn at the start; leftovers stay neutral. After that nobody chooses any more: the scenario card of the winning country decides the next duel (first duel: roulette).
- **Duel:** both countries throw 3 flags at each other's leader; touching the leader ends your turn with 0; closing the triangle gives +200. The loser's country flies the winner's flag. 5 duels, then most countries wins.
- **Text, in English, only where it explains:** a news headline under every scenario card (why these two fight, nations only, nobody quoted) and the leader-hit screen (BOOM!, then WORLD WAR III). New card: Cyber Attack.
- **Duel without the Windows window:** the city video full screen with the target on top; the Windows look stays everywhere else, so the contrast is felt.
- **Every in-between screen moves on by itself** (or with a throw gesture): the player is standing with the phone, away from the laptop.

**Known limits:** the phone ↔ laptop link (PeerJS), the city videos and the currency data cannot be tested from Claude's environment, only on Lorenzo's devices; world map after each duel still to do; brief and README partly outdated; versions v2–v5 use old file names.

**Messages used:** to fill in.

## v7 · 2026-11-23
**Wanted:** the game must explain itself to people who see it for the first time, the phone pairing must not run away, the coin toss must be readable, every country must have its city behind, and the match needs a real ending.

**Decisions (and why):**
- **How to Play screen after the title**, as a Notepad window (`HOW_TO_PLAY.txt`) with lines typed one by one and an icon each. The audience at the presentation has never seen the game; the key rule is spelled out: the closer to the centre, the more points, but never touch the leader.
- **Phone pairing waits for two green ticks:** 1 = phone connected, 2 = webcam sees it. Before, anything pink or a throw gesture skipped the screen before the phone was ready. Mouse icon or Enter = play without a phone (plan B).
- **Coins pile up on gold bars:** each currency stacks coins for how much it grew today against gold (today vs yesterday). The taller pile turns green and throws first, the other red. Same currency (the euro countries) or a censored coin (North Korea) = a coin flipped in the air. The rule was turned around: before, the weaker coin had the advantage, which nobody understood.
- **Videos checked one by one in a real browser:** most backup files did not exist and the USA backup was 8K. Now each city has two tested files (480p and a light 240p); a video that does not start within 8 s is skipped.
- **Riyadh gets a video from YouTube:** the only Riyadh videos on Commons are White House footage with real politicians, against the no-faces rule. An aerial drone video with no people, embedded muted; the channel title and automatic captions are cropped out.
- **Final screen:** the winner's flag, the country's name and WINS! with confetti, then back to the title.
- **Text rule updated:** English text also on the How to Play and WINS! screens.

**Known limits:** very old iPhones (before iOS 17.4) cannot play the Wikimedia videos, the drawn city shows instead; the YouTube video depends on the channel keeping it online; world map after each duel still to do.

**Messages used:** to fill in.

## v8 · 2026-11-24
**Wanted:** after playing a whole match: say who won each battle, show whose turn it is on the phone, a clearer team layout, readable text, a real final screen, and a scoring system where every throw counts until the end.

**Decisions (and why):**
- **Battle result in words:** a banner under the scores (e.g. GERMANY WINS, "Russia goes grey: out of the game"). Before, the points appeared but nobody said who had won.
- **Teams on the sides:** player 1's countries in a column on the left, player 2 on the right, 3 and 4 below; each team header shows its live total. The sidebars work as a scoreboard.
- **Sharper text:** text is drawn on its own layer at 4× resolution, still under the CRT scanlines. The pixel look stays on the graphics, the words become readable.
- **Phone shows the player number (1-4) in the team colour** instead of the flag, so the person holding it knows it is their turn. The link was made self-healing (re-sent every second, auto-reconnect, QR opens the newest page) because on iPhone the number stayed on 1.
- **QR kept square and above the scanlines** so every phone reads it.
- **Score decides the match:** every point goes to the team; the beaten country goes grey instead of changing flag; after 5 duels the top score wins. Winning duels matters, but a close loser is not wiped out.
- **The spare country becomes the LAST CHANCE:** one single throw for the team that is behind, only if it is less than 100 points behind (one flag scores at most 100) and only if that flag covers the gap. Lorenzo's condition: it must not be a gift where far throws win just because of an extra turn.
- **Final screen:** TEAM n WINS! in the team colour, the globe turning into that colour, the team's starting flags orbiting it, STARTED WITH / DEFEATED and every team's total.
- **Coins kept for who throws first:** an energy-price idea for the euro countries was dropped after testing: the service blocks other websites, limits requests and the Italian data licence is private use only.

**Known limits:** the phone number change depends on the phone link (PeerJS), testable only on real phones; world map still to do.

**Messages used:** to fill in.

## Dependency map
| Service | What for | Owned by |
| --- | --- | --- |
| GitHub Pages | hosting | Microsoft |
| Wikimedia Commons | free-licence videos of the capitals | Wikimedia Foundation |
| YouTube (embedded player) | aerial video of Riyadh | Google |
| PeerJS (public server) | phone ↔ laptop link | open-source project |
| qrcode-generator (jsDelivr) | QR code for the phone | open source / jsDelivr |
| currency-api (jsDelivr) | every currency against gold | open source / jsDelivr |
| Open-Meteo | real weather of each capital | Open-Meteo (open data) |
| Higgsfield | character generation | Higgsfield AI |
| Claude | design and code, in dialogue | Anthropic |
