# Reading Habit

The public introduction and user guide for Reading Habit, a private reading tracker for iPhone, iPad, and Mac.

**[Visit the website](https://brianrenshaw.github.io/reading-habit-site/)** · **[Read the guide](https://brianrenshaw.github.io/reading-habit-site/guide/)**

Public app distribution is pending. This repository contains the website and selected sample screenshots, not the application source or a downloadable build.

## Maintain the site

- `index.html` is the app homepage.
- `guide/index.html` is the user guide. Keep its chapter IDs stable so shared links continue to work.
- `assets/styles.css` contains the responsive design. There is no JavaScript, package manager, build step, analytics, or external font dependency.
- `assets/` holds the app icon, favicon, social preview, and screenshots. Screenshots show synthetic simulator data from the September 8, 2026 Reading Habit implementation. The social preview is the existing 1024-pixel app icon, unchanged.

Serve this directory with any static server, or run `python3 -m http.server 8766` in its parent directory and visit `http://localhost:8766/reading-habit-site/`. Serving from the parent tests the same URL prefix as GitHub Pages.

Before publishing an update:

1. Compare instructions with the current app screens and user-facing labels. Check goals, weights, streaks, rest days, the reading-day boundary, and backup/import behavior. Update the guide date when the content changes.
2. Inspect every replacement screenshot for private information and outdated UI. Use sample libraries and illustrative covers.
3. Check both pages at phone and desktop widths, keyboard navigation, contents links, FAQ disclosures, image loading, and direct entry to `/guide/` and chapter anchors.
4. Run `21st review index.html guide/index.html assets/styles.css` if the optional 21st authoring CLI is available. It is not a runtime or deployment dependency.
5. Verify a public release URL before changing the development notice or adding a download button. Update both pages together.

## Publish

GitHub Pages serves the **root of the `main` branch**. `.nojekyll` keeps the HTML and assets unchanged. Push the reviewed files to `main`, wait for the Pages build to finish, and check both public pages without signing in.

The site uses relative internal links so it works under `/reading-habit-site/`. Canonical and social URLs use the public address. If the domain or repository name changes, update those URLs and `sitemap.xml` together.

## Design and content

The site follows the app’s Quiet Depth direction: neutral surfaces, charcoal text, restrained blue, system fonts, and content-led layouts. The approved icon is an open charcoal journal with a blue bookmark on white. The 21st catalog was consulted for landing-page and sidebar patterns; no third-party component code was imported.

Guide content was checked against the current app’s copy, capture, library, reading-history, goal, settings, widget, and Shortcut implementations. Current screen labels take precedence over older help prose. This public repository intentionally excludes developer handoff notes, app identifiers, signing details, private data, and app Git history.

Report a documentation or app problem through this repository’s issues. Issues are public; do not attach a personal library backup.
