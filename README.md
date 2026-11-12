# Klassiker Training Log

Daily plan for En Svensk Klassiker Tjej, 23 Nov 2026 to 26 Sep 2027. Hosted on GitHub Pages.

## Files in this repo (the public app)
- `index.html`: the app and the whole plan
- `plan-updates.json`: plan changes written by Claude after a review (replace this file when you get a new one)
- `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`: make it installable as a phone app

Training log is NOT stored in this repo. It goes in a separate private repo (below), so weight, waist and notes stay private.

## One-time setup
1. **Private data repo.** On GitHub choose New repository, name it `tjejsvenskklassiker-data`, set it to Private, tick "Add a README file", and create it.
2. **Access token.** GitHub, Settings, Developer settings, Personal access tokens, Fine-grained tokens, Generate new token.
   - Repository access: Only select repositories, then pick `tjejsvenskklassiker-data`.
   - Repository permissions: Contents set to Read and write.
   - Expiration: 1 year. Generate, then copy the token (it starts with `github_pat_`).
3. **Connect each device.** Open the app, go to the Progress tab, find "Sync across devices", enter `dibsondivya/tjejsvenskklassiker-data` and paste the token, then press Connect and sync. Do this once on the laptop and once on the phone. The token is saved only in that browser.

After this, ticks, notes and weights upload a few seconds after each change and load when you open the app on any device. The log lives in `progress.json` in the private repo.

## Sending your progress to Claude
In the app, Progress tab, press "Download progress file" (or open `progress.json` in the private repo and download it). Attach it to the chat and ask for a review.

## Getting plan changes back
Claude gives you a new `plan-updates.json`. In this public repo choose Add file, Upload files, drop it in, and commit. Reload the app to see the days marked "Plan adjusted".
