# Antaranga — Daily Tracker

A voice-first daily journal, sadhana/habit tracker, task checklist, hour-by-hour
log, and end-of-day score report — inspired by Reysu's "Life Tracker System".

All your data stays **on your own device**, in the browser's local storage.
Nothing is sent anywhere.

## Files
- `index.html` — the app itself
- `manifest.json` — makes it installable as an app
- `sw.js` — service worker, so it still opens without internet once installed
- `icon-192.png`, `icon-512.png` — app icons

## 1. Publish it on GitHub Pages (free, ~2 minutes)

1. Create a new **public** repository on GitHub, e.g. `antaranga`.
2. Upload all 5 files in this folder to the repository (drag-and-drop on the
   GitHub website works fine — "Add file" → "Upload files").
3. Go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a URL like:
   `https://YOUR-USERNAME.github.io/antaranga/`
   (takes a minute or two to go live the first time).

## 2. Install it on your phone (Chrome, Android)

1. Open that URL on your phone in **Chrome**.
2. Tap the **⋮** menu (top right) → **"Add to Home screen"** or **"Install app"**.
3. It now opens full-screen from your home screen, like any other app —
   no browser bar, works offline, has its own icon.

(On iPhone, use Safari's **Share → "Add to Home Screen"** instead — voice
input support varies by iOS version.)

## 3. Using it

- **Today** tab — one-line highlight of the day, sadhana/habit tracker
  (tap = done, double-tap = skipped), and your main tasks for the day.
- **Hours** tab — a note for every hour, speak it in with the mic icon, and
  tag it 🟢 productive / 🔴 doom-scroll or wasted / grey untagged — tap the
  small circle to cycle through.
- **Journal** tab — tap the big mic and just talk; it transcribes straight
  into your journal entry for the day.
- **Report** tab — today's score: +1 per productive hour/task/habit, −0.9 per
  wasted hour or skipped task/habit. Toggle between a line chart (the shape
  of your day, like the "energy graph" in the video) and a bar chart
  (per-hour breakdown).
- **Goals** tab — your goals for the current month.

Swipe/tap the ‹ › arrows at the top to move between days.

## Notes

- Voice input uses the browser's built-in speech recognition
  (`webkitSpeechRecognition`). It works well in Chrome; support in other
  browsers varies. If it's unavailable, you can always type instead.
- Data is stored per-browser using `localStorage`. If you use both your
  phone and a laptop, they'll have separate journals — there's no sync
  built in. (Let me know if you'd like that added — it would need a small
  backend or a service like Firebase.)
