# IronStart PWA — first working version

A small offline-first Android workout planner. It uses plain HTML/CSS/JavaScript to keep the first version easy to inspect and modify. Workout data is saved in the browser's localStorage; no account or server database is used.

## Programme in this version
- Workout A: squat 3×5, bench press 5×5, deadlift 1×5
- Workout B: squat 3×5, overhead press 5×5, barbell row 5×5
- Three non-consecutive sessions per week is a suggested schedule; the app alternates A/B whenever a session is saved.
- Complete every prescribed rep target: increase the next load by the exercise increment.
- Miss any target reps: repeat that load next time. Three misses are a cue to consider a 10% reset and review recovery/technique; the app does not automatically deload.
- Loads are total bar weight, not per-side plate weight.

## Run locally
Service workers and PWA installation require HTTPS or localhost. For a quick local test with Python installed:
1. Unzip the package.
2. In this folder run `python -m http.server 8000`.
3. Open `http://localhost:8000` on the same device or computer.

For phone installation, deploy the folder to any static HTTPS host (for example, GitHub Pages, Netlify, or Cloudflare Pages). Open the HTTPS URL in Chrome on Android, use the browser menu, and choose **Install app** or **Add to Home screen** (wording varies).

## Before using for real
- Check starting weights with a qualified coach if unsure; choose a load you can control with good technique and no pain.
- The default barbell starts are suggestions only. A standard 20 kg bar may be too heavy for some beginners; a lighter training bar or dumbbells may be more appropriate.
- Export a JSON backup regularly. Browser data can be erased by clearing site data, uninstalling, or losing the device.
- The app is a starter prototype: it does not yet have a custom icon, automated reminder notifications, cloud sync, warm-up calculator, or a dedicated per-set numeric keypad.
