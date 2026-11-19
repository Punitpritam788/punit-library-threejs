Punit's Library | One Bookcase. Three Tiers.
<p align="center">
  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML"><img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"></a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/CSS"><img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"></a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/JavaScript-ES_Modules-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111111" alt="JavaScript ES Modules"></a>
  <a href="https://threejs.org/"><img src="https://img.shields.io/badge/Three.js-0.185.0-000000?style=for-the-badge&logo=threedotjs&logoColor=white" alt="Three.js 0.185.0"></a>
  <img src="https://img.shields.io/badge/Rendering-WebGL-990000?style=for-the-badge" alt="WebGL">
  <img src="https://img.shields.io/badge/Architecture-Single%20HTML%20File-6B4F3A?style=for-the-badge" alt="Single HTML file">
  <img src="https://img.shields.io/badge/Build%20Step-Not%20Required-2E7D32?style=for-the-badge" alt="No build step required">
</p>An interactive 3D portfolio built as a dark-walnut library. Instead of presenting projects as a conventional grid of cards, the experience invites visitors into a wooden study, where personal chapters, GitHub projects, manga and manhwa, games, and collectible objects live on three browsable shelves.

Built with: HTML, CSS, JavaScript ES modules, and Three.js
Creator: Punit Pritam Mohanty
GitHub profile: github.com/Punitpritam788
One Bookcase. Three Tiers. A portfolio you can explore.

Contents
- What is this?
- Highlights
- Technology
- Run locally
- How to explore
- Catalogue customization
- Architecture and maintainer notes
- Live data and fallbacks
- Privacy and limitations
- Troubleshooting
- Before you publish changes
- GitHub repository setup
What is this?
Punit's Library is a single-page, full-screen 3D portfolio and personal archive. The room itself is the navigation system: visitors begin with a ceiling-level introduction, move down to the walnut bookshelf, select individual volumes, and inspect their details on information panels inlaid into the wooden floorboards.

The catalogue combines professional work and personal interests. The three tiers are deliberately different, but share one interaction model:
Tier	Collection	Included in the built-in catalogue
01 - Projects & Chapters	Personal story and skills volumes, selected concepts, and curated GitHub repositories	30 volumes: 7 personal chapters, 2 concept projects, and 21 repository entries
02 - Manga & Manhwa	Japanese manga and Korean manhwa, with separate reading directions	22 volumes
03 - Games & Discs	PS5/PC game cases, artwork, spinning optical discs, and gaming collectibles	16 fallback titles


The displayed counts can change after live GitHub or game-trend synchronization. The numbers above describe the embedded starting catalogue, not a permanently fixed online total.
Highlights
A 3D room, not a flat portfolio template
- An original wooden study with a pitched ceiling, dark walnut surfaces, brass details, and a three-tier bookshelf.
- A cinematic ceiling introduction that zooms into the bookshelf.
- Three independently focusable shelves with horizontally browsable contents.
- Individual books and game cases that can be pulled out and opened.
- Clickable details and actions rendered directly onto the wooden floorboard texture.
- A landscape-view suggestion on tall screens, with an option to continue in portrait.
Tier 01 - Projects & personal chapters
- Personal volumes describe background, skills, work experience, interests, and career direction.
- Concept volumes introduce selected experiments and game ideas.
- Curated GitHub repositories have individual shelf entries, repository links, and optional live-demo links.
- The searchable repository directory provides a separate way to find projects.
- GitHub synchronization can add public repositories and refresh their metadata.
- Repository README text can be fetched to enrich descriptions when the shelf entry is opened.
Tier 02 - Manga & manhwa
- A catalogue of 22 manga/manhwa entries.
- Filters for all titles, manga, and manhwa.
- Cover artwork is looked up from public catalogue services when available.
- Japanese manga use a right-to-left hinge and page direction; Korean manhwa use a left-to-right direction.
- A book-cover animation and two-page spread preview demonstrate the appropriate reading direction.
- Optional official reading links are shown separately from the preview.
Important: the spread reader is a visual interaction preview with generated sample text. It does not contain scanned manga/manhwa pages and is not a full digital reading service.
Tier 03 - Games, cases & collectibles
- PS5 and PC categories with platform filters.
- Detailed 3D game cases, cover artwork, spines, backs, manuals, and optical-disc labels.
- A bookshelf presentation and a separate CD-carousel mode.
- An animated disc-insertion sequence.
- Three-dimensional gaming collectibles, including showcase objects such as a Cyberpunk-style relic, a CS2-inspired Karambit, and a Dota 2 Aegis.
- A manual trend update that attempts to refresh game entries and artwork from public sources.
Platform labels in the trend feed are best-effort classifications. They should not be treated as a verified compatibility or store-availability database.
Technology
Technology	Role
HTML5	Semantic page structure, overlays, navigation controls, and modal interfaces
CSS3	Walnut/brass visual system, responsive HUD, overlays, transitions, and reduced-motion rules
JavaScript ES modules	Application state, catalogue parsing, user interaction, data fetching, and orchestration
Three.js 0.185.0	WebGL scene, camera, room and shelf geometry, books, cases, collectibles, raycasting, and animation
Canvas 2D	Procedural wood and cover textures, floorboard artwork, inlaid text, and texture composition
Browser APIs	fetch, localStorage, Pointer Events, touch input, ResizeObserver, Clipboard API, and media queries


There is no framework runtime, bundler, package manifest, backend server, or required API key in this delivery.
Run locally
Requirements
- A modern desktop or mobile browser with JavaScript ES modules, import maps, Canvas 2D, and WebGL support.
- Hardware acceleration/WebGL enabled.
- Internet access for the Three.js CDN and optional live repository, catalogue, image, and game-trend services.
The room and its initial contents are generated from the embedded catalogue. If a remote data provider is unavailable, the built-in catalogue and available local cache are used. The Three.js module itself is loaded from a CDN, so the 3D scene still requires that dependency to be reachable.
Start a local static server
Place the HTML file in a folder, open a terminal in that folder, and run:
python -m http.server 8000
On Windows, py -m http.server 8000 may be used instead.

Open the filename in your browser, for example:
http://localhost:8000/punit_library_three_tier_walnut_bookshelf_documented.html
Use an HTTP server rather than opening the file through file://; browser module and cross-origin behavior is more predictable when served locally.
Deploy
The app is a static page. For GitHub Pages, place the HTML file in the published root (or the selected Pages folder), rename it to index.html if you want it to load as the site's default page, and enable Pages for that branch/folder. No build command is required. Any other static host serving the file over HTTPS can be used as well.
How to explore
On-screen controls
- Ceiling Intro - return to the opening camera view.
- Bookshelf - show all three tiers.
- 01 Projects / 02 Manga / 03 Games - focus one tier.
- Floor Details - move to the wooden floorboard detail view.
- Prev / Next - move between items in the active tier.
- Pull / Open - pull a selected volume or case out, open it, and return it to the shelf through repeated activation.
- Return - clear the current selection or return from floor details.
- Sync - refresh public GitHub repository information.
- Update Trends - try to refresh the PS5/PC game collection.
- All GitHub Repos - open the searchable repository directory.
- Insert Disc - play the game-disc insertion animation.
The Tools group contains collection-specific filters and display modes. On smaller screens, the secondary controls can be expanded or collapsed.
Mouse and touch
Input	Action
Click/tap a book or game case	Select it; click it again to return it
Click/tap a 3D collectible	Select it for close inspection
Drag horizontally across a shelf	Browse the shelf contents
Drag a pulled-open case	Rotate the case
Drag a selected collectible	Rotate the collectible
Pinch or use the mouse wheel on a selected collectible	Zoom the collectible
Swipe vertically or use the page wheel/trackpad	Move between ceiling, bookshelf, and floor
Swipe in the spread reader	Turn the preview spread in the correct reading direction


Keyboard
The page-level shortcuts are ignored while typing in an input or textarea, and modal-specific controls take priority.
Key	Action
← / →	Previous / next item in the active tier
↑ / W	Move up through the room levels; when a tier is focused, move toward the previous tier first
↓ / S	Move down through the room levels; when a tier is focused, move toward the next tier first
PageUp / PageDown	Move one room level up/down
F	Toggle Floor Details / Bookshelf
C	Toggle Ceiling Intro / Bookshelf
Enter / Space	Enter the library from the intro, or pull/open the current item
Escape	Close the active modal/reader, return from floor details, clear a selection, or restore all tiers depending on the current state


Catalogue customization
The initial content is embedded in:
<script type="application/json" id="catalog-data">
  { ... }
</script>
Edit the JSON inside this element to change the starting catalogue. Keep the element ID and valid JSON syntax. Do not add JavaScript comments or trailing commas inside the JSON.
Top-level catalogue keys
Key	Type	Purpose
personalBooks	Array	Personal story, skills, experience, and career volumes
conceptBooks	Array	Selected project and concept chapters
projectNotes	Object	Repository-specific display metadata, keyed by GitHub repository name
projectOrder	Array of strings	Preferred order for the curated repository shelf
mangaBooks	Array	Manga/manhwa metadata, identifiers, cover lookup fields, and reading direction
gameData	Array	Fallback game catalogue, platform tags, links, and artwork information


Personal and concept books
A typical personal/concept volume uses:
{
  "title": "The Builder's Toolkit",
  "author": "Punit Pritam Mohanty",
  "genre": "craft",
  "series": "My Story",
  "note": "A concise description displayed on the floorboard detail panel."
}
The title, author, series, and note are display fields. genre is descriptive metadata in the current catalogue; it is not a built-in shelf filter.
Project notes and order
Each projectNotes value is an array containing a preferred series label, description, and an optional demo URL:
{
  "my-project-repository": [
    "Worlds & Play",
    "A concise description of the project.",
    "https://example.com/live-demo/"
  ]
}
Add the corresponding repository name to projectOrder to control its position among the curated repositories. Keep the names aligned with the actual GitHub repository names. When live GitHub data is available, the app enriches matching entries and can append additional public, non-fork, non-archived repositories.
Manga/manhwa entries
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
  "note": "A short description of the series.",
  "officialReadUrl": "https://example.com/official-series-page",
  "officialSource": "Official Publisher"
}
- format is descriptive (manga or manhwa).
- rtl controls the cover hinge and spread navigation direction. Use true for right-to-left volumes and false for left-to-right volumes.
- anilistId is used for an exact AniList lookup when present. Otherwise, search and optional country are used for title search. malId supports the Jikan/MyAnimeList fallback path.
- spineColor is a fallback visual color.
- h and d influence generated book proportions. The renderer clamps dimensions to safe shelf ranges, so extreme values will not be preserved exactly.
- officialReadUrl and officialSource are optional links/labels; they do not supply content to the local spread preview.
Game entries
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
- caseType should be ps5 or pc to participate in the built-in platform filters and styling.
- title, tag, platform, accent, and note supply the visible case/detail content.
- appId enables additional Steam artwork candidates.
- cover and fallbackCover are image candidates.
- store and optional psStore are outbound links.
- source is a display/provenance label.
Architecture and maintainer notes
The application is delivered as one HTML file containing markup, CSS, JSON data, and a JavaScript module. The module intentionally does not export a public JavaScript API. The supported customization points are the embedded catalogue and the DOM controls described above; internal classes and functions are implementation details, not stable external contracts.
Component	Responsibility
#catalog-data	Local-first starting dataset
UnifiedHouseLibrary	Three.js scene, camera, room/shelf construction, object state, raycasting, input, and animation
FloorboardDetailRenderer	Canvas-based details and clickable action regions mapped onto the floorboard
renderUnifiedUI(state)	Connects scene state to DOM controls, floating actions, modals, and floorboard content
initialise()	Populates the room, wires controls, starts remote hydration, warms up rendering, and dismisses the loader


Scene state model
The UI callback receives a state object shaped like:
{
  viewMode: 'ceiling' | 'bookshelf' | 'floor',
  tier: 0 | 1 | 2,
  focusTier: 'all' | 0 | 1 | 2,
  item: Object | null,
  collectible: Object | null,
  state: 'shelved' | 'pulled' | 'opened' | 'launching',
  gamesMode: 'bookshelf' | 'carousel'
}
The selection lifecycle is shared by books and game cases: shelved → pulled → opened, with another activation returning the item to the shelf. Collectible selection is maintained separately so 3D objects can be rotated and zoomed without pretending they are book entries.
Canvas floorboard actions
The detail panel is drawn into a canvas texture rather than built from ordinary HTML buttons. Button labels and action regions are painted together; the renderer stores their corresponding UV hit areas. When the floorboard is clicked, the scene raycasts the surface and dispatches the callback for the matching region. Keep each button's onClick callback attached to its display specification when extending this renderer.
Procedural layout and performance
- Shelf placement variations use deterministic hashing so the same catalogue produces a repeatable arrangement.
- The initial room is built from local data before network enrichment completes.
- Remote image work uses a bounded concurrency pool; compact screens use lower texture/image settings than larger screens.
- Renderer pixel ratio, texture scale, anisotropy, and shadow quality are adjusted using screen/device heuristics.
- The initial loading process has an early-entry option and a 12-second cap while waiting for external asset tasks; remaining requests can continue updating the scene afterward.
- prefers-reduced-motion disables selected nonessential motion effects and CSS transitions.
Live data, external services, and fallbacks
All external requests run in the visitor's browser against public endpoints. There is no API key or private credential embedded in the page.
Feature	Sources used by the implementation	Fallback behavior
GitHub projects	GitHub REST API for public repositories; raw GitHub README files for descriptions	Curated catalogue, then last locally cached repository snapshot
Manga/manhwa covers	AniList GraphQL, followed by Kitsu and Jikan/MyAnimeList fallback lookups	Generated cover/spine artwork from the local entry
PS5 trends	PlayStation Blog WordPress API, parsing a Top Downloads post	Embedded game catalogue or cached trend snapshot
PC/Steam trends	Steam featured categories through public CORS proxies; CheapShark deals/game lookup	Embedded game catalogue or cached trend snapshot
Game artwork	Steam and other image candidates supplied by the catalogue/data providers	Procedurally generated case artwork and textures
Image resizing	wsrv.nl image proxy	Original image URL is also tried


Two browser localStorage keys are used for snapshots:
- punit_library_gh_repos_v1 - GitHub repository data.
- punit_library_trending_games_v1 - game trend data.
The stored values include a savedAt timestamp, but the current code does not enforce a cache expiry period. Clear either key in browser storage to discard that snapshot and force the built-in/online fallback path on the next sync.

Game-platform trend detection is heuristic. The app parses a PlayStation blog post and uses a curated cross-platform keyword pattern to classify some Steam titles. Results and store destinations can be incomplete or misclassified; verify platforms and store links independently before relying on them.
Privacy and limitations
- No account, sign-in, analytics SDK, or backend service is required by the supplied HTML.
- Public repository and catalogue requests are made from the browser; the browser stores only the described repository/game snapshots in localStorage.
- The Three.js engine is CDN-hosted, so an offline-first fully disconnected launch is not supported by the current import map.
- Missing third-party artwork does not remove the local shelf entries, but the visual result may use generated fallback textures.
- The experience requires WebGL; there is no static 2D scene fallback.
- The spread reader is a directional UI preview, not an archive of copyrighted pages.
- The current delivery does not include an automated test suite or build pipeline; browser/manual checks are required after changes.
Troubleshooting
Problem	Things to check
Blank scene or module error	Serve over HTTP/HTTPS, confirm the Three.js CDN is reachable, enable hardware acceleration, and inspect the browser console for import/WebGL errors.
Loader reports that the engine is taking too long	Check connectivity to the CDN and reload. A startup watchdog displays a reload option if the module does not boot in time.
Books appear without remote covers	The local data loaded, but a cover provider, image host, or CORS proxy may be unavailable. Try syncing again later.
GitHub list does not refresh	Use Sync GitHub. If the request fails, the app uses its cached snapshot or built-in catalogue. Clear punit_library_gh_repos_v1 to remove the saved snapshot.
Game list appears unchanged	Use Update Trends. If providers are unavailable, the app uses cached trends or the embedded gameData. Clear punit_library_trending_games_v1 to remove the saved snapshot.
Mobile shelves feel cramped	Use landscape orientation for the intended wide layout, or dismiss the suggestion and continue in portrait.
A project has no live-demo action	Add a third URL element to its projectNotes entry or provide a valid repository homepage/GitHub Pages URL.


Before you publish changes
1. Validate the JSON inside #catalog-data.
2. Keep projectOrder entries aligned with actual repository names and projectNotes keys.
3. Confirm every manga/manhwa has the correct rtl value and a valid optional official link.
4. Use caseType: "ps5" or caseType: "pc" for game entries.
5. Preserve the DOM IDs and data-* attributes used by the interaction wiring.
6. Test a desktop landscape viewport and a mobile/touch viewport.
7. Check the console and manually try one project, one manga/manhwa item, one game case, a collectible, floorboard actions, both modals, and the remote-sync fallback path.
GitHub repository setup

The badge row at the top of this README reflects the implementation: HTML5, CSS3, JavaScript ES modules, Three.js 0.185.0, WebGL, a single HTML file, and no required build step. No license, deployment, CI, or automated-test badge is included because those statuses are not established by the supplied source.
Made with curiosity, code, and a little walnut polish.
