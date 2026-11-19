<div align="center">

# Punit's Library

**An interactive 3D personal archive built as a three-tier walnut library.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-Explore_the_Library-d8a94c?style=for-the-badge)](https://punitpritam788.github.io/punit-library-threejs/)
[![GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-2f473b?style=for-the-badge&logo=github&logoColor=white)](https://punitpritam788.github.io/punit-library-threejs/)
[![Three.js](https://img.shields.io/badge/Three.js-0.185.0-111111?style=for-the-badge&logo=threedotjs&logoColor=white)](https://threejs.org/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES_Modules-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111111)](https://developer.mozilla.org/docs/Web/JavaScript)

*One Bookcase. Three Tiers. A portfolio you can explore.*

</div>

Punit's Library replaces the usual portfolio grid with an original, full-screen 3D wooden study. Enter the room, descend from a cinematic ceiling view, and browse a dark-walnut bookshelf containing projects, manga and manhwa, games, discs, and 3D collectibles.

The experience is implemented in a **single `index.html` file** with no framework, build step, package manifest, or backend.

---

## Explore the Library

### Tier 01 — Projects & Chapters

- 7 personal story and skills volumes
- 2 concept and experiment volumes
- 21 curated GitHub repositories
- Project details, repository links, demos, and README summaries
- A searchable GitHub repository directory
- Optional live synchronization with public GitHub repository data

### Tier 02 — Manga & Manhwa

- 22 embedded catalogue entries
- Separate Manga (RTL) and Manhwa (LTR) filters
- Animated cover opening and directional two-page spread preview
- AniList, Kitsu, and MyAnimeList/Jikan cover lookup fallbacks
- Optional links to official publisher or reading pages

> The spread reader is a visual preview using generated sample text. It does not contain scanned pages or provide a digital reading service.

### Tier 03 — Games, Discs & Collectibles

- 16 fallback PS5 and PC game cases
- Platform and layout filters
- Generated and remotely sourced cover artwork
- Spinning optical discs and an animated disc-insertion sequence
- PS5/PC bookshelf and CD-carousel modes
- 3D collectibles, including Cyberpunk-style, CS2-inspired, and Dota-inspired showcase objects
- Optional live trend refresh for PS5 and PC titles

---

## Highlights

- Cinematic ceiling introduction that zooms into the bookshelf
- Three independently focusable tiers
- Pull-out, open, return, and close interactions for books and game cases
- Horizontal shelf browsing with mouse, touch, or keyboard
- Procedural walnut textures and wood surfaces rendered with Canvas 2D
- Canvas-rendered floorboard details with clickable action regions
- Responsive HUD for desktop and mobile layouts
- Landscape guidance for narrow or tall screens
- Reduced-motion support
- Local cache and embedded fallbacks when live services are unavailable

---

## Live Links

| Resource | Link |
| --- | --- |
| Live site | https://punitpritam788.github.io/punit-library-threejs/ |
| Repository | https://github.com/Punitpritam788/punit-library-threejs |
| GitHub profile | https://github.com/Punitpritam788 |

---

## Run Locally

### Requirements

- A modern desktop or mobile browser
- JavaScript ES modules and WebGL support
- Hardware acceleration enabled
- Internet access for the Three.js CDN and optional live data providers

### Start a static server

From the repository root:

```bash
python -m http.server 8000
```

Windows users may also use:

```bash
py -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

Use a static HTTP server instead of opening `index.html` through `file://` so browser module and cross-origin behavior remain predictable.

---

## Controls

### Mouse and touch

| Action | Result |
| --- | --- |
| Click or tap an object | Select a book, case, or collectible |
| Click or tap again | Return or clear the selection |
| Drag horizontally across a shelf | Browse items |
| Drag a pulled case or collectible | Rotate it |
| Pinch or mouse wheel over a collectible | Zoom it |
| Swipe vertically / use the wheel | Move between room levels |
| Swipe in the manga reader | Turn the preview spread |

### Keyboard

| Key | Action |
| --- | --- |
| `←` / `→` | Previous / next item |
| `↑` / `W` | Move up in the room |
| `↓` / `S` | Move down in the room |
| `PageUp` / `PageDown` | Change room level |
| `F` | Toggle floor details |
| `C` | Toggle the ceiling intro |
| `Enter` / `Space` | Enter the library or pull/open an item |
| `Escape` | Close overlays or clear the current selection |

The on-screen HUD also provides direct controls for the ceiling, shelf tiers, floor details, item navigation, GitHub synchronization, trend updates, repository search, filters, and game-disc controls.

---

## Technology

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure, overlays, controls, and dialogs |
| CSS3 | Walnut/brass theme, responsive HUD, transitions, and reduced motion |
| JavaScript ES Modules | State, catalogue, interaction, networking, and scene orchestration |
| Three.js 0.185.0 | WebGL room, camera, geometry, raycasting, animation, and meshes |
| Canvas 2D | Procedural wood textures, cover artwork, floorboard rendering, and actions |
| Browser APIs | `fetch`, `localStorage`, Pointer Events, ResizeObserver, clipboard access, and media queries |

There is no framework runtime, bundler, backend, or required API key.

---

## Catalogue Customization

The starting catalogue is embedded in `index.html` inside:

```html
<script type="application/json" id="catalog-data">
  <!-- ... -->
</script>
```

Top-level keys include:

| Key | Purpose |
| --- | --- |
| `personalBooks` | Personal story and skills volumes |
| `conceptBooks` | Concept and experiment volumes |
| `projectNotes` | Repository descriptions and optional demo URLs |
| `projectOrder` | Preferred curated-repository order |
| `mangaBooks` | Manga/manhwa metadata and reading direction |
| `gameData` | Fallback PS5 and PC catalogue |

Keep the JSON valid: do not add comments or trailing commas. Keep repository names in `projectOrder` aligned with `projectNotes` and GitHub's repository names.

### Personal or concept volume

```json
{
  "title": "The Builder's Toolkit",
  "author": "Punit Pritam Mohanty",
  "genre": "craft",
  "series": "My Story",
  "note": "A concise description shown in the floorboard detail panel."
}
```

### Manga or manhwa volume

```json
{
  "title": "Example Series",
  "author": "Creator Name",
  "format": "manga",
  "rtl": true,
  "anilistId": 12345,
  "malId": 123,
  "search": "Example Series",
  "country": "JP",
  "spineColor": "#c86428",
  "h": 1.54,
  "d": 0.22,
  "note": "A short description.",
  "officialReadUrl": "https://example.com/official-series-page",
  "officialSource": "Official Publisher"
}
```

Use `rtl: true` for manga-style right-to-left navigation and `rtl: false` for left-to-right manhwa-style navigation.

### Project note

```json
{
  "my-project-repository": [
    "Worlds & Play",
    "A concise description of the project.",
    "https://example.com/live-demo/"
  ]
}
```

The third array element is an optional live-demo URL.

### Game entry

```json
{
  "title": "Example Game",
  "tag": "PC · Steam",
  "platform": "PC · Steam",
  "caseType": "pc",
  "accent": "#b83b2e",
  "appId": 123456,
  "cover": "https://example.com/cover.jpg",
  "fallbackCover": "https://example.com/fallback.jpg",
  "store": "https://store.steampowered.com/app/123456/",
  "psStore": "https://store.playstation.com/",
  "note": "A short description.",
  "source": "Steam"
}
```

Use `caseType: "ps5"` or `caseType: "pc"`.

---

## Live Data & Fallbacks

Public data is requested from the visitor's browser. The page does not embed private credentials or API keys.

| Feature | Provider | Fallback |
| --- | --- | --- |
| GitHub repositories | GitHub REST API and raw README files | Embedded catalogue and local cache |
| Manga/manhwa covers | AniList, Kitsu, Jikan/MyAnimeList | Generated cover and spine artwork |
| PS5 trends | PlayStation Blog WordPress API | Embedded catalogue and local cache |
| PC/Steam trends | Steam and public deal/game services | Embedded catalogue and local cache |
| Game artwork | Catalogue artwork candidates | Procedurally generated textures |

Repository and trend snapshots are stored in browser `localStorage`:

- `punit_library_gh_repos_v1`
- `punit_library_trending_games_v1`

Clear these keys to discard saved snapshots and restore embedded/current on-demand data.

Platform labels and trend classifications are heuristic, not a verified game compatibility or store-availability database.

---

## Architecture

The app follows a state-driven single-file structure:

| Component | Responsibility |
| --- | --- |
| `#catalog-data` | Embedded, local-first starting data |
| `UnifiedHouseLibrary` | 3D scene, camera, room, shelves, raycasting, state, and animation |
| `FloorboardDetailRenderer` | Canvas floorboard details and clickable action regions |
| `renderUnifiedUI(state)` | DOM controls, floating actions, modals, and scene-state updates |
| `initialise()` | Catalogue population, control wiring, live hydration, rendering, and loader dismissal |

The selection lifecycle for books and cases is:

```text
shelved → pulled → opened
```

A later activation returns the item to the shelf. Collectible selection and carousel state are maintained separately.

---

## Privacy & Limitations

- No account, sign-in, analytics SDK, or backend is required.
- Public repository and catalogue requests are made from the browser.
- The Three.js module is loaded from a CDN, so a fully offline launch is not currently supported.
- Missing artwork is replaced with generated fallback textures.
- WebGL is required; there is no static 2D scene fallback.
- The manga/manhwa reader is not a copyrighted page archive.
- This project does not currently include an automated test suite or build pipeline.

---

## Troubleshooting

| Problem | Check |
| --- | --- |
| Blank scene or module error | Serve over HTTP/HTTPS, enable hardware acceleration, and inspect the browser console |
| Loader takes too long | Confirm CDN connectivity and reload; the startup watchdog provides a reload option |
| Missing remote covers | The embedded catalogue should remain visible; provider availability or CORS may be the issue |
| GitHub repos do not refresh | Use **Sync GitHub** or clear `punit_library_gh_repos_v1` |
| Trends do not update | Use **Update Trends** or clear `punit_library_trending_games_v1` |
| Mobile shelf feels cramped | Switch to landscape or widen the browser window |
| Project has no demo action | Add a third URL to its `projectNotes` entry |

---

## Publishing Checklist

1. Validate JSON inside `#catalog-data`.
2. Align `projectOrder`, `projectNotes`, and real GitHub repository names.
3. Confirm Manga/Manhwa `rtl` values and official links.
4. Use `caseType: "ps5"` or `caseType: "pc"` for game entries.
5. Preserve DOM IDs and `data-*` attributes used by interaction code.
6. Test desktop landscape and mobile/touch layouts.
7. Test project, manga, game, collectible, floorboard, modal, and live-sync fallback paths.

---

<div align="center">

Made with curiosity, code, and a little walnut polish.

**Creator:** [Punit Pritam Mohanty](https://github.com/Punitpritam788)

</div>
