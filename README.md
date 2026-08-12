# 70th Ohio State Convention Interactive Guide

A responsive, accessible, single-file static website for the 70th Ohio State Convention schedule and floor plan.

## Files

- `index.html` — the complete website, including styles, schedule data, SVG floor plan, and JavaScript.
- `.nojekyll` — tells GitHub Pages to serve the static files directly.

No build step, package manager, framework, or external CSS/JavaScript library is required.

## Publish with GitHub Pages

### Replace the existing page

1. Open the `Interactive-OSC` repository on GitHub.
2. Replace the repository-root `index.html` with this `index.html`.
3. Add the empty `.nojekyll` file.
4. Commit the changes to the branch currently used by GitHub Pages, usually `main`.

If the repository already publishes with GitHub Pages, the existing site should update after the commit.

### Configure a new repository

1. Create a repository and upload `index.html`, `.nojekyll`, and this `README.md` to its root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch and the `/(root)` folder, then save.
5. The site address will use the form `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

## Local preview

You can double-click `index.html`, or serve the folder locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Updating the schedule

Open `index.html` and find the `EVENTS` array near the bottom. Each schedule item is defined once. The page automatically uses that data to:

- render the selected day's schedule;
- search events, rooms, and people;
- highlight rooms on the SVG map;
- build each room's complete event list;
- create shareable URL fragments for events.

## Improvements over the earlier version

- Removed Tailwind CDN and Google Fonts dependencies.
- Replaced duplicated hand-written schedule markup and room lookup data with one source of truth.
- Added keyboard-accessible map rooms and day tabs.
- Added schedule search, deep links, copy-link support, print styling, reduced-motion support, and clearer mobile behavior.
- Split Friday hospitality, literature, and archives into their correct rooms.
- Expanded panel titles and speaker/moderator details from the official schedule.
