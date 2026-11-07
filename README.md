# PlayGround

<!-- omgithub:readme:start -->
## 🚀 Build, play, and remix with OMGithub

**Created using [OMGithub.com](https://go.ondev.store/).**

[![OMGithub](https://img.shields.io/badge/OMGithub-Open%20project-orange?style=for-the-badge)](https://go.ondev.store/InnovativeUG/PlayGround)
[![GitHub](https://img.shields.io/badge/GitHub-Source-181717?logo=github&style=for-the-badge)](https://github.com/InnovativeUG/PlayGround)

- 🎮 [Open the project](https://go.ondev.store/InnovativeUG/PlayGround).
- ✨ [Remix this project](https://go.ondev.store/InnovativeUG/PlayGround?remix=1).
- 💻 [Explore the source](https://github.com/InnovativeUG/PlayGround).
- 🛠️ [Check build runs](https://github.com/InnovativeUG/PlayGround/actions).
- 🐛 [Report an issue](https://github.com/InnovativeUG/PlayGround/issues).
- 👤 [Explore the creator's projects](https://go.ondev.store/InnovativeUG).
- 🌍 [Create with OMGithub](https://go.ondev.store/).
<!-- omgithub:readme:end -->

## Utility Empire — Field Operations

A browser-based, third-person utility-work career sim set in Pacifica. Explore Harbor Bay, take a work order, collect equipment, travel by truck, and carry out the authorized field steps with your crew.

### Run locally

Serve the project directory with any static HTTP server, then open its local URL in a modern browser. `index.html` loads Three.js 0.160.0 from jsDelivr using an import map, so an internet connection is needed for the Three.js CDN (and for the optional Google Fonts). There is no project build step or npm package manifest.

### Controls

- **WASD** — move; **Shift** — run
- **E** — interact; **F** — enter or exit the vehicle
- **V** — change camera view; **M** — map; **Tab** — career panel; **R** — dispatcher radio
- Touch controls are provided on small screens.

### Rendering and visual scope

The game uses **Three.js 0.160.0 with `THREE.WebGLRenderer` and WebGL**. It is not built on Unreal Engine, does not use WebGPU, and does not provide a path-traced renderer. The scene uses Three.js mesh geometry and standard materials, real-time directional shadows, ACES filmic tone mapping, fog, and a simple time-of-day and weather cycle (clear, rain, and overcast). Rendering is capped at a device-pixel ratio of 1.8 to limit pixel workload. Appearance and performance vary with the browser, device, and available WebGL implementation.

Workers are currently **stylized procedural PPE characters**, assembled from simple meshes in `game.js`. Walking and the foreperson's work motion use basic limb rotations; they are not realistic human models or motion-captured animation. The repository also contains `public/models/human-rigged.glb`, but the game does not currently load it. Its accompanying asset metadata reports no textures and no animation clips, so it is not a finished realistic animated character. Character dialogue has no facial animation or lip sync.

### Dialogue and voice limitations

Text dialogue is the reliable fallback; replies are handled by the game's local scripted logic, not a connected AI service. Microphone input is offered only when the browser exposes `SpeechRecognition` or `webkitSpeechRecognition`; availability and permissions vary by browser and device. When a reply follows recognized speech, the game can use the browser's `speechSynthesis` API to read it aloud if available. This is browser-provided speech, not recorded character voice acting, and it is not synchronized to character mouths. If voice APIs are unavailable or denied, use the conversation text field.

