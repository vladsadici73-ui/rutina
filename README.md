# Rutină

A local-first weekly routine planner built for iPad. Lay out tasks for each day of the week, set up recurring tasks (daily or on specific weekdays), and check things off as you go — no account, no backend, no internet required after the first load.

Built with a blueprint/schematic-inspired look: grid background, color-coded task "wires," and segmented progress indicators per day.

## Features

- **Week view** — swipeable day-by-day carousel, one page per weekday
- **One-off tasks** — add a task for a specific day directly from that day's view
- **Routines** — create recurring tasks and choose which weekdays they repeat on (or toggle "Daily" for all 7)
- **Color-coded routines** — each recurring task gets a color so it's easy to recognize at a glance
- **Progress tracking** — completion count and segmented progress bar for each day
- **Local persistence** — data is saved with `localStorage`, so it survives closing and reopening the app

## Tech

Single-file app — plain HTML, CSS, and vanilla JavaScript. No build step, no dependencies, no framework. Fonts (Space Grotesk, IBM Plex Sans, IBM Plex Mono) are loaded from Google Fonts.

## Running it locally

1. Download `rutina_etapa3.html`
2. Open it directly in Safari (or any browser)
3. On iPad: tap Share → **Add to Home Screen** to use it like a real app, fullscreen, with an icon

## Deploying it (so others can access it via a link)

The app needs to be hosted somewhere to get a public link. A few options:

- **[Netlify Drop](https://app.netlify.com/drop)** — rename the file to `index.html` and drag it in, get an instant link
- **GitHub Pages** — push `index.html` to a repo, enable Pages in Settings, get `https://<username>.github.io/<repo>/`
- **Vercel** — similar drag-and-drop or GitHub-connected deploy

> **Note:** Data is stored per device/browser via `localStorage`. Each person who opens the link has their own independent task list — nothing is shared or synced between users. Adding shared/synced data would require a backend.

## Project stages

This app was built in three stages, each kept as its own file:

| File | What it adds |
|---|---|
| `rutina_etapa1.html` | Visual foundation — theme, layout, week navigation, swipeable day carousel (no task data yet) |
| `rutina_etapa2.html` | Task data model, checkboxes, add/delete tasks per day, `localStorage` persistence |
| `rutina_etapa3.html` | Recurring routines — repeat on chosen weekdays or daily, color-coded, full app |

## Roadmap / ideas

- Weekly/monthly stats and streaks
- Drag-and-drop task reordering
- Local notifications/reminders
- JSON export/import for backup
- Convert to a real PWA (manifest + service worker) for full offline support
