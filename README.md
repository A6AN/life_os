# Life OS — GitHub Pages tracker

A zero-build, mobile-first, installable static web app. No frameworks, backend, tokens, or subscription.

## Deploy

1. Create a GitHub repository, e.g. `life-os` (private repositories may have Pages restrictions depending on your plan; check GitHub's current Pages settings).
2. Upload **index.html, app.js, styles.css, seed.json, sw.js, icon.svg, manifest.webmanifest** to the root. `build_seed.py` is optional and not required at runtime.
3. In repo **Settings → Pages**, set **Deploy from a branch**, branch **main**, folder **/(root)**, then save.
4. Open the Pages URL on Samsung S23 in Chrome. Use Chrome's menu → **Add to Home screen** / **Install app**.
5. Keep updating tasks, events and syllabus directly in the app. Your edits and checkmarks are stored in browser storage on that device, not GitHub. **Export JSON backups** from Settings. Import the backup on a different browser/device.

## Updating content without editing code

- Today: press **+ Add** under events or study tasks, and **⋯** to edit/delete existing entries.
- Week: **+ Next week** creates blank days; weekly care tasks still appear automatically. It never guesses future classes. Tap a day to add classes or tasks. **Copy tasks from another day** for reusable focus plans.
- Mastery: select **Not started / In progress / Exam-ready** after closed-book problem solving. **+ Unit** adds missed or new course topics.
- Projects: edit next action or deadline when known.
- Settings: edit care routine, travel buffers, scratchpad and export/import progress.
- Each selected day has a specific prompt with classes, travel cues, active study tasks, health reminders, and explicit no-duplicate and no-invented-times rules.

## Updating the default shared plan

`seed.json` contains `days` keyed by `YYYY-MM-DD`, `syllabus`, and `projects`. Edit it in GitHub to change defaults for **new users**. Existing app users keep their local edited data; updates to seed won't overwrite checkmarks and tasks. To load a changed default on your own browser, first export a backup, then use Settings → Reset local data (which clears local progress).

## Privacy / limitations

GitHub Pages serves static files. Your local edits are not synced across devices and cannot be edited from GitHub just by checking a task in your browser. Reinstalling or clearing site data can remove progress; export backups. The service worker caches the app for offline use **after an online visit**. Browser permissions determine whether the app installs. Copying a phone-assistant prompt does not itself schedule reminders.

Attendance and exams are sourced from the uploaded class and exam schedules. Neuroscience syllabus is missing. Project deadlines, mess times and medication dosing are not invented. No unverified minoxidil+finasteride dosing reminders. All generated dates use Asia/Kolkata language/context; device date navigation follows the device's local date.
