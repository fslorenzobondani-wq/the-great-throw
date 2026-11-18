# The Great Throw

A circus throwing game where the targets are the world's most powerful leaders — and you throw flags, not knives.

Nine faceless, censored politician-mannequins are strapped to a spinning red-and-white circus wheel. You plant your flags around them without touching them: close the circle and you win; graze the leader and the system crashes. Behind the wheel runs the real camera of the capital's square. Every win changes a shared world map and makes two linked countries react.

No words in the game: only icons, flags, colours and numbers.

## How to play
- **Laptop** = the target screen. Open the page and click to start.
- **Phone** = the thrower. Scan the QR code on the title screen, then swipe up to throw, left/right to pick.
- **Solo mode:** click on the wheel, or use the arrow keys and Enter.

## Real-world data
- **Who starts:** today's coin. Each currency is measured against gold since yesterday; the weaker coin gets the advantage (the wheel starts still). Same currency (the four euro countries) → a coin toss. North Korea has no free market rate: its coin is censored.
- **Weather and local time** of each capital drive the fallback background.
- **Soundtrack:** `audio/soundtrack.mp3`, with a real visualiser in the taskbar; on a crash the song slows down and dies like a jammed tape.

## City videos (credits)
Behind each duel plays a free-licence video of the capital from Wikimedia Commons; the local hour tints it (night, dusk) and real rain is drawn on top. Change them in `NATIONS[...].video` in `index.html`.

| Capital | Video on Wikimedia Commons |
| --- | --- |
| Rome | [Fontaine de Trevi.webm](https://commons.wikimedia.org/wiki/File:Fontaine_de_Trevi.webm) |
| Madrid | [Puerta del Sol, 2012.webm](https://commons.wikimedia.org/wiki/File:Puerta_del_Sol,_2012.webm) |
| Paris | [Eiffel tower 141853 1.webm](https://commons.wikimedia.org/wiki/File:Eiffel_tower_141853_1.webm) — Quahadi |
| Berlin | [Demo von Wikimedia und F5 … vor dem Brandenburger Tor 02.webm](https://commons.wikimedia.org/wiki/File:Demo_von_Wikimedia_und_F5_gegen_das_Sicherheitspaket_vor_dem_Brandenburger_Tor_02.webm) |
| Washington | [2025-12-17 White House ballroom construction Washington DC 11-23-28 1.webm](https://commons.wikimedia.org/wiki/File:2025-12-17_White_House_ballroom_construction_Washington_DC_11-23-28_1.webm) |
| Moscow | [A view of Red Square MVI 6782.ogv](https://commons.wikimedia.org/wiki/File:A_view_of_Red_Square_MVI_6782.ogv) |
| Beijing | [天安门等地下半旗悼念李克强同志.webm](https://commons.wikimedia.org/wiki/File:天安门等地下半旗悼念李克强同志.webm) — China News Service |
| Pyongyang | [Donny Ferguson - 360 degree view of Pyongyang … Juche Tower.webm](https://commons.wikimedia.org/wiki/File:Donny_Ferguson_-_360_degree_view_of_Pyongyang,_North_Korea,_from_atop_the_Juche_Tower.webm) — Donny Ferguson |
| Riyadh | no free video found: drawn city |

Each file keeps its own licence (see its Commons page).

## Files
- `index.html` — the whole game
- `img/` — character sprites
- `audio/soundtrack.mp3` — the soundtrack
- `process.md` — versions, decisions and dependency map
- `versions/` — saved versions

Vibe Coding final project · Elisava MAIAD 26/27.
