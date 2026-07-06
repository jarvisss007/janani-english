# ಜನನಿ · Janani — English for Amma

A Kannada-first English course for mothers. Built originally for my own mother moving from Karnataka to the U.S. — now personalized for any learner: enter your name, choose what matters to you (travel, doctor, phone calls, shopping…), and the course reshapes itself around your goals and learns from every answer you give.

**Live app:** https://jarvisss007.github.io/janani-english/

## What it is

A single-file web app (no server, no accounts, no tracking) that teaches functional English to a Kannada speaker:

- **12 parvas (chapters), 35 lessons** — alphabet, introductions, phone calls, airport, shopping, health, daily life
- **Five exercise types** — choose the meaning, tap what you hear, build the sentence, match pairs, say it aloud
- **Adaptive review** — every answer is tracked; a daily *abhyasa* session drills the weakest words
- **Kannada-first UI** with audio (device text-to-speech, Indian-English accent by default)
- **Installable PWA** — add to home screen, works fully offline after first load
- Progress, streaks and settings stored locally on the device only

## Structure

| File | Purpose |
|---|---|
| `index.html` | The entire app (HTML + CSS + JS, self-contained) |
| `manifest.json` | PWA manifest (installability) |
| `sw.js` | Service worker (offline cache) |
| `icon-192.png`, `icon-512.png` | App icons |

## Run locally

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Publishing

Play Store launch kit is ready — see [PLAY_STORE.md](PLAY_STORE.md) for the step-by-step guide.
Store assets (icon, feature graphic, phone screenshots) live in [store-assets/](store-assets/).
Privacy policy: [privacy.html](privacy.html).

## Roadmap

- Google Play release (kit ready — see PLAY_STORE.md)
- Deeper Level 2–4 content; native-speaker review of Kannada
- Recorded family voice instead of TTS
- More languages: Hindi, Tamil, Telugu
