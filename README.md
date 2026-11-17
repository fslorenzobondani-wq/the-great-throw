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

## Set up the live cams
In `index.html`, each nation in `NATIONS` has `live: ''`. Paste the YouTube ID (the part after `watch?v=`) of a live cam of that square.

## Files
- `index.html` — the whole game
- `img/` — character sprites
- `audio/soundtrack.mp3` — the soundtrack
- `process.md` — versions, decisions and dependency map
- `versions/` — saved versions

Vibe Coding final project · Elisava MAIAD 26/27.
