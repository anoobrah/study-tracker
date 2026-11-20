# Study Tracker

A small installable web app for planning study **by the week**:

- **This week**: on Monday, add the topics you'll study. At the end of the week, mark each one *Done*, *Partly* or *Not done* (with an optional reason). Unfinished items carry over to next week with one tap.
- **Courses**: every 2-1 course with its lecture topics and a progress bar. Tap a status to change it, tap a name to rename it, ↗ opens the slides.
- **History**: how much of each week's plan actually got done.

Live at **https://anoobrah.github.io/study-tracker/**. Open it in Chrome on your phone, then **⋮ → Add to Home screen / Install app**.

Data is saved on the device only (localStorage). Use **Courses → Settings & backup → Download backup** now and then.

## "Check Drive for new slides" (one-time setup)

The topics found on 20 Nov 2026 are built in. To pick up new slides from the shared `2-1 CSE'24` Drive folder, the app needs a free Google API key:

1. Go to <https://console.cloud.google.com/>, create a project (any name).
2. **APIs & Services → Library →** search **Google Drive API → Enable**.
3. **APIs & Services → Credentials → Create credentials → API key**. Copy it.
4. (Recommended) Edit the key: *Application restrictions → Websites* → add `https://anoobrah.github.io/*`; *API restrictions → Google Drive API*.
5. In the app: **Courses → Settings & backup** → paste the key → **Save key**.

The key only reads files that are shared by link. New topics show up with a **NEW** tag; file names like `Chapter 4.pdf` come in as-is, so tap to rename them.

## Files

`index.html` (the whole app), `manifest.webmanifest`, `sw.js` (offline cache), `icons/`.
