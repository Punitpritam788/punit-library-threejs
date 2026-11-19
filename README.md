<div align="center">

# 📚 Punit's Library — Three-Tier Walnut Bookshelf

### *One Bookcase. Three Tiers. Zero Build Step. Pure 3D WebGL.*

[[https://img.shields.io/badge/Three.js-0.185.0-000000?style=for-the-badge&logo=threedotjs&logoColor=white]](https://threejs.org/)
[[https://img.shields.io/badge/WebGL-3D_Study-d8a94c?style=for-the-badge&logo=webgl&logoColor=1a100a]](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
[[https://img.shields.io/badge/ES_Modules-Vanilla_JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=1a100a]](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[[https://img.shields.io/badge/Architecture-Single_HTML_File-3e5b4d?style=for-the-badge&logo=html5&logoColor=white]](#)
[[https://img.shields.io/badge/Mobile_%26_Desktop-Optimized-9c2b35?style=for-the-badge&logo=responsive&logoColor=white]](#)
[[https://img.shields.io/badge/GitHub-Punitpritam788-181717?style=for-the-badge&logo=github&logoColor=white]](https://github.com/Punitpritam788)

**An interactive, full-screen 3D dark-walnut study room where your portfolio, GitHub projects, favorite manga/manhwa, and live trending PS5 & PC games live on a three-tier wooden bookcase—with every detail inlaid directly into the hardwood floorboards.**

[🌐 Live Demo](https://punitpritam788.github.io/[REPO-NAME]/) · [📂 GitHub Profile](https://github.com/Punitpritam788) · [🐛 Report a Bug](https://github.com/Punitpritam788/[REPO-NAME]/issues)

</div>

---

## ✨ What Makes It Different

Instead of a flat card grid, **Punit's Library** drops you inside a cozy, wood-paneled 3D study room—starting from the vaulted timber rooftop intro, sweeping down into a handcrafted three-tier dark-walnut bookcase, and angling down to an interactive hardwood floorboard ledger.

### 🏛️ Three Interactive Shelf Tiers
- **Tier 01 · Projects & Personal Chapters (`30+` volumes):** Personal story chapters paired with **live-synced GitHub repositories** (`Punitpritam788`). Pull any book to open its chapter notes, jump straight to the repo or live demo, or browse all repositories in the searchable directory modal.
- **Tier 02 · OG Manga & Manhwa (`22` volumes):** Geometrically accurate **Right-to-Left (RTL)** Japanese manga (hinged on the right spine) and **Left-to-Right (LTR)** Korean manhwa (hinged on the left spine) with live cover fetching (AniList / Kitsu / MAL), an interactive 3D spread reader, and **verified official reading links** (VIZ Media, Kodansha, Dark Horse Digital, WEBTOON, Tappytoon, Tapas).
- **Tier 03 · Trending Games & CDs (PS5 + PC):** Hinged 3D **PlayStation 5 Blu-ray** and **PC Steam** cases with spinning optical discs, a **CD Carousel** mode, an **Insert Disc** animation, **All / PS5 / PC** filters, official store/download links, and **Update Trends ↻** to fetch live trending PC & PS5 charts online and regenerate every cover, 3D spine, back cover, booklet, and disc label on the fly.

### 🗿 Sculpted 3D Shelf Collectibles & Study Environment
- **8 Procedural 3D Collectibles:** Super Saiyan Goku & 4-Star Dragon Ball, Guts' Dragon Slayer greatsword, One Piece Thousand Sunny ship, Sung Jin-Woo's 3-tier daggers, PlayStation 5 Disc Edition & DualSense, Cyberpunk 2077 Relic 2.0 biochip case, CS2 Karambit Fade + C4, and Dota 2 Collector's Aegis—all using the same **tap-to-pull, drag-to-rotate 360°, tap-to-return** mechanism as books and CDs.
- **Real-Time Local-Clock Lighting:** The study dynamically shifts across **Dawn, Daylight, Golden Hour, and Night Study** based on your local time—updating the window sky, sunbeam shaft, directional sunlight, brass lamps, and the antique wall clock's live hands.
- **Modern PC Corner & Atmospheric Details:** Heritage striped library walls, fluted pilasters with brass sconces, three bookcase picture lamps, drifting golden dust motes, bump-mapped floorboards, and a partially visible dark-walnut PC battlestation (curved ultrawide IDE display, tempered-glass PC with spinning fans, and gaming chair).

### ⚡ Performance & Mobile-First Engineering
- **Theme-Matched Asset Loader + Pre-Scroll GPU Warmup:** Tracks 3D scene construction, GitHub sync, 22 manga covers, and 16 game covers, then sweeps the camera across **Floor → Bookshelf → Ceiling** while pre-compiling WebGL shaders so scrolling responds with zero hitch the instant you enter.
- **Adaptive Device Scaling:** Automatically scales procedural canvas textures, cover proxy sizes, shadow maps, and pixel ratio for smaller devices, pauses the render loop when the tab is hidden, collapses secondary controls on short landscape phones, and suggests horizontal view on tall vertical screens.

---

## 🎮 Controls

| Action | Desktop / Laptop | Mobile / Touch |
| :--- | :--- | :--- |
| **Move Ceiling ↔ Bookshelf ↔ Floor** | Mouse Wheel / Trackpad / `↑` `↓` / `W` `S` / `PageUp` `PageDown` / Right `▲ ▼` Rail | Vertical Swipe / Right `▲ ▼` Rail |
| **Browse Shelf Horizontally** | Hover across shelf or Drag Left/Right | Horizontal Swipe on Shelf |
| **Pull / Open / Return Volume or 3D Model** | Click spine or 3D model (`Enter` / `Space` / `Esc`) | Tap spine or 3D model |
| **Inspect 360° Model or Opened Game Case** | Click & Drag (`Scroll` to zoom) | Drag to Rotate / Pinch to Zoom |
| **Flip Manga / Manhwa Spreads** | `←` / `→` Arrows or Click Cover | Swipe Left / Right |

---

## 🛠️ Tech Stack

- **3D Engine:** Three.js (`0.185.0` via ES Module Import Map)
- **Textures & UI Inlays:** 100% Procedural HTML5 Canvas 2D (wood grain, book spines, covers, UV-mapped interactive floorboard ledger, monitor IDE screen, live wall clock)
- **Live Data Integrations:** GitHub REST API, AniList GraphQL / Kitsu / Jikan, Steam / CheapShark / PlayStation Blog
- **Packaging:** Single self-contained `.html` file—no bundler, no `node_modules`, instant deploy to GitHub Pages

---

## 🚀 Run Locally

```bash
git clone [https://github.com/Punitpritam788/](https://github.com/Punitpritam788/)[REPO-NAME].git
cd [REPO-NAME]
# Serve with any static server (or open directly via Live Server)
python3 -m http.server 8000
