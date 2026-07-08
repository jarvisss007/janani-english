# 📦 Publisher Handoff — ಜನನಿ Janani (English for Amma)

This document is for the person publishing Janani on their Google Play account.
Everything is already built and hosted — your job is only the Play Store side.
Total effort: ~1 hour of clicking + Google's waiting periods.

**The app:** https://jarvisss007.github.io/janani-english/
**Source:** https://github.com/jarvisss007/janani-english
**Contact for anything:** Anupam (repo owner)

---

## What this app is (30 seconds)
A free English-learning course for Kannada-speaking mothers. It is a PWA
(Progressive Web App): the Play Store app is a thin wrapper around the live
website above. It collects **no data** — no accounts, no analytics, no ads.
All learner progress stays on the user's device.

Because it's a wrapper, **app updates never require a new store upload** —
content and features update through the website automatically.

---

## Step 0 — Your Play developer account
- If you already have one: skip ahead. **Note:** accounts created before
  Nov 2023, or that have already published an app, may not need the
  "12 testers for 14 days" closed-test requirement — check whether
  Play Console asks for it. If not required, you can go straight to production.
- If you need one: https://play.google.com/console/signup → "Yourself" →
  $25 one-time → identity verification (ID + a card-charge code, normal).

## Step 1 — Generate the Android package (10 min, no coding)
1. Go to https://www.pwabuilder.com
2. Enter: `https://jarvisss007.github.io/janani-english/`
3. **Package for Stores → Android**, with:
   - Package ID: `io.github.jarvisss007.janani`
   - App name: `Janani — English for Amma`
   - Short name: `Janani` · Version: `1.0.0`
   - Signing key: **Create new**
4. Download the ZIP. Inside:
   - the **`.aab`** — the file you upload to Play
   - the **signing keystore + passwords** — ⚠️ save these in two places and
     **send a copy to Anupam**. Losing the keystore = the app can never be updated.
   - **`assetlinks.json`** — **send this file to Anupam immediately**; he must
     host it on the website (removes the browser bar). The app is fine to
     upload before this is done, but do it before production.

## Step 2 — Create the app in Play Console
Play Console → **Create app**
- App name: `Janani — English for Amma`
- Default language: English (US) · **App** · **Free**
- Declarations: not a news app, contains no ads

## Step 3 — Store listing (all copy-paste)
- **Short description:**
  `Learn English from Kannada — a gentle, personalized course made for mothers.`
- **Full description:** copy the block from
  [PLAY_STORE.md](PLAY_STORE.md) (section "Full description")
- **App icon:** `icon-512.png` (in the repo root)
- **Feature graphic:** `store-assets/feature-graphic.png`
- **Phone screenshots:** the 3 PNGs in `store-assets/`
- **Category:** Education
- **Privacy policy URL:** `https://jarvisss007.github.io/janani-english/privacy.html`
- **Contact email:** yours (or Anupam's — agree between you)

## Step 4 — Questionnaires (exact answers)
**Content rating** → category Education → answer **No** to everything
(violence, sexual content, profanity, drugs, gambling, user-generated
content, location, personal-info sharing) → result: Everyone / 3+.

**Data safety** →
- Collect or share any user data? → **No**
- (The optional AI tutor only activates if a user pastes their own API key;
  it is off by default and disclosed in the privacy policy.)

**Target audience** → **18 and over** (adult learners).

**Ads** → No ads.

## Step 5 — Upload & release
1. If closed testing is required for your account: **Testing → Closed testing**
   → upload the `.aab` → add 12 testers (family/friends emails) → they install
   via the opt-in link → wait 14 days → apply for production.
   If not required: **Production → Create release** directly.
2. Upload the same `.aab`, write release notes (`First release`), **Send for review**.
3. Review typically takes 1–7 days.

## What to send back to Anupam
- [ ] `assetlinks.json` (from the PWABuilder ZIP) — immediately
- [ ] A backup copy of the keystore + its passwords — for safekeeping
- [ ] The Play Store listing URL once live 🎉

## Ongoing
Nothing. App updates flow through the website with no store action.
The only future store task: Google occasionally (about yearly) requires a
target-SDK bump — re-run PWABuilder with the same keystore and upload.

---
*Built by Anupam Patil for his mother. Thank you for helping it reach every Amma.* 🪔
