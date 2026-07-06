# 🚀 Play Store Launch Guide — ಜನನಿ Janani

Everything is prepared. Your part takes ~45 minutes + Google's review time (typically 1–7 days).

---

## Step 1 — Create the developer account ($25, one-time)
1. Go to https://play.google.com/console/signup
2. Sign in with your Google account → choose **"Yourself"** (personal account)
3. Pay the **$25 one-time** registration fee
4. Complete identity verification (they may ask for an ID — normal)

## Step 2 — Generate the Android app package (no coding)
We use **PWABuilder** (Microsoft's free tool) — it wraps the live site into a signed Android app:
1. Go to https://www.pwabuilder.com
2. Enter: `https://jarvisss007.github.io/janani-english/`
3. Click **Package for Stores → Android**
4. Settings to use:
   - **Package ID:** `io.github.jarvisss007.janani`
   - **App name:** `Janani — English for Amma`
   - **Short name:** `Janani`
   - **Version:** `1.0.0`
   - Signing key: **"Create new"** (let PWABuilder generate it) — **download and keep the .keystore file + passwords safely** (Google Drive backup!). Losing it means you can never update the app.
5. Download the ZIP → it contains the **`.aab`** file (the app) and **`assetlinks.json`**

## Step 3 — Send me the assetlinks.json
The `assetlinks.json` from the ZIP must be hosted at
`https://jarvisss007.github.io/janani-english/.well-known/assetlinks.json`
— give me the file (or its SHA-256 fingerprint) and I'll add it to the repo and push. Without it, the app shows a browser bar on top.

## Step 4 — Create the app in Play Console
Play Console → **Create app**:
- Name: `Janani — English for Amma`
- Default language: English (US) — (Kannada listing can be added as a translation)
- App type: **App** · Free
- Declarations: not a news app, no ads

### Store listing (copy-paste ready)
- **Short description** (max 80 chars):
  `Learn English from Kannada — a gentle, personalized course made for mothers.`
- **Full description:**

```
ಜನನಿ · Janani teaches practical English to Kannada speakers — designed with love for mothers joining their families abroad.

WHY JANANI
• Everything in Kannada first — you never need English to use the app
• Enter your name and your goals (travel, doctor, phone calls, shopping…) and the course rebuilds itself around YOU
• Your name is woven into the lessons — learn to say "My name is …" with your real name

A COMPLETE 4-LEVEL COURSE
• Level 1 · Survival (A1) — alphabet, introductions, airport, doctor, shopping
• Level 2 · Daily life (A2) — past & future, directions, feelings, appointments
• Level 3 · Conversation (B1) — experiences, opinions, solving problems
• Level 4 · Confidence (B2) — natural expressions and deeper conversation

LEARN THE WAY THAT WORKS
• 5 exercise types: choose the meaning, tap what you hear, build the sentence, match pairs, say it aloud
• Every phrase shown in English, Kannada meaning, and pronunciation written in Kannada script — with audio
• The app tracks every answer and a daily review (ಅಭ್ಯಾಸ) drills your weakest words
• Practice real conversations with Guru — at the shop, at the doctor, on a call with your son

MADE FOR COMFORT
• Large text with size control, gentle sounds, dignified design
• Works fully offline after the first load
• No account, no ads, no tracking — your progress never leaves your phone

ಪ್ರತಿ ದಿನ ಒಂದು ಪಾಠ ಸಾಕು. One lesson a day is enough.
```

- **App icon:** upload `icon-512.png` (in the repo)
- **Feature graphic:** upload `store-assets/feature-graphic.png`
- **Phone screenshots:** upload the 3 PNGs in `store-assets/`
- **Category:** Education
- **Contact email:** your email
- **Privacy policy URL:** `https://jarvisss007.github.io/janani-english/privacy.html`

### Content rating questionnaire (answers)
Category: **Education** → answer **No** to everything (no violence, no sexual content, no profanity, no drugs, no gambling, no user-generated content, no location sharing, no personal-info sharing) → rating comes out **Everyone / 3+**.

### Data safety form (answers)
- Does your app collect or share any of the required user data types? → **No**
- Is all of the user data collected by your app encrypted in transit? → N/A (nothing collected)
- Do you provide a way for users to request that their data is deleted? → N/A
(The optional AI tutor sends chat text to Anthropic only if the user adds their own key — Google's form counts this as user-initiated, not app collection; it is disclosed in the privacy policy.)

### Target audience
- Target age: **18 and over** (it's for adults; avoids children's-app requirements)

## Step 5 — Upload & release
1. **Testing → Internal testing** → upload the `.aab` → add your own email as tester → verify it installs and opens on your phone
2. Then **Production → Create release** → same `.aab` → **Send for review**
3. Review usually takes 1–7 days. You'll get an email when it's live.

---

## Checklist of what's already done ✔
- [x] Live HTTPS site (GitHub Pages) with service worker + offline
- [x] Web manifest with id, icons (192/512, maskable), category
- [x] Privacy policy page (privacy.html)
- [x] Feature graphic 1024×500 (store-assets/)
- [x] 3 phone screenshots 1080×2340 (store-assets/)
- [x] Store listing copy, rating & data-safety answers (this file)
- [ ] $25 account — **you**
- [ ] PWABuilder package + keystore — **you** (10 min)
- [ ] assetlinks.json → send to me, I push it
- [ ] Upload + submit — **you**
