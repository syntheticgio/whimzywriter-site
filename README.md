# WhimzyWriter Website

The website for **WhimzyWriter**, a native macOS writing app. GitHub Pages serves this repository's `main` branch at <https://syntheticgio.github.io/whimzywriter-site/>. It's plain HTML and CSS with no build step; `.nojekyll` turns off Jekyll.

## Pages

| Path | Content |
|---|---|
| `index.html` | Home: overview, an app-window mock showing an AI diff under review, first-run steps, and what's coming later |
| `editor/` | Writing: projects, chapters and scenes, snapshots, the editor, paragraph styles, spellcheck, search, export |
| `agents/` | AI tools: providers, chat, inline rewrites and whole-text tools, review and authorship, semantic search |
| `world/` | World building: codex, outline board, timeline, notes |
| `philosophy/` | Principles: AI never changes text silently, AI is optional, work stays on your Mac, native Mac app |

Shared files: `css/site.css` (one stylesheet, light and dark), `js/site.js` (the small-screen menu), and `assets/` (app icons copied from the app's asset catalog).

## Design

- **Palette:** cool lilac paper (`#f4f3fb`), indigo ink (`#211c40`), violet accent (`#5646d6`). Marigold (`#e3a33a`) is used only for AI-authorship marks and inserted text, matching how the app shows AI changes. Dark-mode values are in `site.css`.
- **Type:** Fraunces for headings and the manuscript in the window mock; Figtree for everything else. Both load from Google Fonts.
- **Layout:** each section is a "chapter" with its heading in a side column and prose beside it, collapsing to one column on small screens. Features are plain definition lists or tables rather than cards.
- **Motion:** one animation on the home page, where the diff in the window mock appears. It's turned off when reduced motion is requested.

## Keeping it accurate

Describe only what the app implements. The sources of truth live in the app repository: `apps/whimzywriter/README.md`, the plan in `apps/whimzywriter/plans/` (decisions §2, milestones §7) and the specs in `apps/whimzywriter/specs/`. Features from later milestones go under "Coming later" on the home page.

Don't add pricing, release dates or an App Store link until they exist. WhimzyWriter isn't open source, so the site doesn't link to the app's source code.

## Previewing

Open `index.html` in a browser, or serve the folder so the relative links resolve like they do on Pages:

```bash
python3 -m http.server 8080
```
