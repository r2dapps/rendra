<div align="center">

```
 ┌─────────────────────────────────────────┐
 │      ◢■◣   R E N D R A   ◢■◣            │
 │   SketchUp  ──►  Lumion-style world     │
 │                  ──►  GLB, offline      │
 └─────────────────────────────────────────┘
```

### `#ECECE6` Studio Chalk &nbsp;·&nbsp; `#141519` Obsidian Ink

**Open a `.skp`. Light it like a film set. Export a `.glb`. No install, no server, no upload.**

`Three.js 0.170` · `OpenSKP` · `GLTF/GLB` · `PWA` · `Offline-first` · `Zero build step`

<br/>

[![Live Demo](https://img.shields.io/badge/Live%20Demo-r2dapps.github.io%2Frendra-2b825b?style=for-the-badge&logo=googlechrome&logoColor=white)](https://r2dapps.github.io/rendra/)
[![PWA Ready](https://img.shields.io/badge/PWA-Offline%20Ready-141519?style=for-the-badge&logo=pwa&logoColor=ECECE6)](https://r2dapps.github.io/rendra/)

</div>

---

## ✦ What is RENDRA?

RENDRA is a single-page 3D studio that runs entirely in your browser. Drop a SketchUp file in, and it is converted on your own device. Nothing is sent anywhere. You then inspect, measure, section, light and film it, and export a clean GLB.

The visual language is two colors only: chalk and ink, with frosted-glass panels floating over your model. Day and night themes are the same palette, inverted.

---

## ✦ What's new in this edition

| Layer | Addition |
|---|---|
| **Director dock** | A floating cinematic bar at the bottom of the viewport |
| **Looks** | One-click presets: *Noon · Golden Hour · Blue Hour · Overcast · Rain Storm · Snowfall* |
| **Weather** | Clear, Mist (volumetric-style fog), Rain (streaks), Snow (drifting flakes) that follow your camera target |
| **Exposure + Grade** | Live exposure slider, vignette and film grain |
| **Cinematic Tour** | Auto orbit with dolly and crane motion. Touch the canvas to take over |
| **Photo** | One-click PNG capture of the viewport |
| **Film** | Record the canvas to `.webm` at up to 12 Mbps, tour starts automatically |
| **Clean mode** | Hides all UI for pure-image shots |
| **True PWA** | Real manifest, service worker, PNG and SVG icons, install button, full offline use after first load |

The existing engine is untouched: SKP→GLB conversion, 180° solar arc, procedural Lumion world (terrain, roads, traffic, pool, lamps, trees), section planes, x-ray, clay mode, tape measure, 2D floor-plan slice and the explode and assemble animation.

---

## ✦ v4 — Lumion World+, editor-grade focus

| Area | What changed |
|---|---|
| **Sky** | Real gradient sky dome that follows the sun: twilight → golden → noon, with a sun glare and weather-aware greying |
| **Clouds** | Drifting cloud banks that warm at sunrise and grey out in mist, rain and snow |
| **Terrain** | The blob hills are replaced by a sculpted mountain ring. It is coloured by altitude (meadow → forest → rock → snow) and keeps valleys open along the roads |
| **No more overlaps** | Cars, lamps and trees that would intersect your loaded model are removed, and traffic lanes that cross it are dropped |
| **Selection** | Single-click selects a part and shows a **blue bounding box** (visible through walls, with a translucent fill and corner studs). Click empty space to deselect |
| **Focus** | `F` or `.` focuses the selection (or frames everything), `Home` frames all, double-click focuses a part, and the dock has **Focus** and **Frame** buttons |
| **2D plan** | Clicking the plan now selects and flies to the **nearest part** under that spot |
| **Measure** | Tape points, line and endpoints are **blue** |
| **Clean mode** | A **Show UI** pill stays at the top; `Esc` or `Shift+H` also brings everything back |

## ✦ v5 — FX pipeline & polish

| Area | What changed |
|---|---|
| **FX panel** | New **FX** button in the dock: a post-processing pipeline with toggles for ambient occlusion (GTAO), bloom, depth of field (auto-focus on the orbit target) and FXAA |
| **Color grade** | Five looks: Neutral, Warm Arch, Cool Nordic, High Contrast and Film |
| **Hi-res stills** | Photo can be 1x, 2x or 4x, capped to your GPU's texture limit |
| **MP4 recording** | Records MP4 (H.264) where the browser supports it, otherwise WebM |
| **Saved views** | **Views** button: save camera bookmarks (kept in localStorage), click to fly, right-click to delete |
| **World** | Scale figures (people), an animated normal-mapped pool, and glass with proper reflections (IOR, clearcoat) |
| **SKP Textures** | Embedded textures are now correctly preserved on import via OpenSKP `{ textures: true }` |

## ✦ v6 — Architectural Demo Villa Estate & Engine Stability

| Area | What changed |
|---|---|
| **Demo Villa Estate** | Full 240-mesh luxury modern villa estate with 1.80m concrete perimeter wall, motorized slatted driveway gate, pedestrian wicket door, covered pergola carport, parked sedan, and stepping stone walkway |
| **Furnished Interiors** | Ground floor living lounge (sectional sofa, coffee table, acoustic media wall, OLED screen), 8-seater dining table with linear chandelier, chef's kitchen with Nero Marquina waterfall island, and powder room. Upper floor master suite (king bed, duvet, nightstands, lamps), dressing wardrobe, en-suite bath (freestanding tub, double vanity, glass shower), and executive study |
| **PBR Textures** | Procedural canvas textures for Honed Nero Marquina marble, warm woven linen fabric, and granite cobblestone pavers |
| **Engine Bugfixes** | Fixed sky dome shader directive newline parsing, wireframe blackscreen defect, altitude color array clamp, and drawer FX slider bindings |
| **2D CAD Plan Slicing** | Planimetric slicing at 1.76m elevation dynamically renders the estate boundary, gate openings, interior walls, and furniture layouts |

## ✦ v7 — True HDRI Sky & Image-Based Lighting (IBL)

| Area | What changed |
|---|---|
| **HDRI Presets** | Instant switching between **Daylight** (Clear sky, 14.5° elev), **Overcast** (Soft architectural studio, 12.0° elev), and **Sunset** (Golden hour rim lighting, 17.2° elev) |
| **Offline & CDN Fallback** | Local HDR assets precached in `assets/hdri/*.hdr` via Service Worker `rendra-v10` for 100% offline access, with automatic CDN fallback |
| **Custom HDR Import** | Load any `.hdr` or `.exr` file directly from local disk via the studio file picker |
| **Lighting & Optics Controls** | Real-time sliders for **IBL Exposure** (0.2x to 3.0x), **Sky Blur / Defocus** (0.00 to 0.60), and **Sky Azimuth** (0° to 360°) |
| **Sky Dome Isolation** | Toggle **Sky Dome** on/off to retain accurate physical reflections on glass, marble, and automotive paint while presenting a clean neutral or Rayleigh background |
| **Sun & Compass Sync** | Dragging the Lumion compass slider dynamically synchronizes the 360° HDR environment dome and reflections with directional sun casting |
| **Single Source of Truth** | Fully coordinated state between the Lumion World drawer, Post-Processing FX panel, and bottom Director dock |

Not yet done: PBR texture sets (external maps), billboard vegetation, geo sun study, first-person walk, self-hosting libraries and instancing.

## ✦ Quick start

```bash
# any static server works; a service worker needs http(s) or localhost
npx serve .            # or:  python3 -m http.server 8080
```

Open `http://localhost:8080`, then use your browser's **Install** option (or the **Install** button in the dock) to add it as an app.

> Opening `index.html` straight from disk (`file://`) still works. You just won't get the service worker or install prompt.

---

## ✦ v8 — Studio HDRI IBL, WASD First-Person Walk, Volumetric Lighting & AEC PBR Library

| Capability | Implementation |
|---|---|
| **Studio HDRI Sky & IBL** | True high dynamic range image-based lighting with Equirectangular HDR textures (`daylight`, `overcast`, `sunset`), live IBL exposure (`0.2x`–`3.0x`), sky defocus blur (`0.00`–`0.60`), 360° azimuth rotation, sky dome isolation toggle, and custom `.hdr`/`.exr` loading |
| **First-Person WASD Walk** | Architectural eye-level (1.65m) navigation with WASD/arrow locomotion, `Shift` sprint (7.0 m/s), `Space` jump, and mouse look. Ground-penetrating raycaster dynamically climbs entrance pavers, plinth slabs, and staircase treads with gravitational free-fall |
| **Volumetric Street Lighting** | Curbside luminaire poles equipped with physical volumetric light cones (`THREE.AdditiveBlending`) and ground illumination pools that dynamically brighten during dusk, sunset, and night |
| **AEC PBR Pre-Library** | 10 curated architectural finishes (*Brushed Travertine, Nero Marquina, Board-Formed Concrete, Teak Timber, Fluted Glass, Corten Steel, Brushed Titanium, Terrazzo Bianco, Ceramic Mosaic, Acoustic Felt*) with procedural PBR maps |
| **Zero-Overhead Lazy Loading** | Material textures are generated strictly on demand when clicked, keeping initial page load memory overhead at absolute zero |
| **Atomic Material Reset** | Single-click "Reset Part" and "Reset All Parts" restore individual elements or all 240 estate meshes to their pristine SketchUp materials |

---

## ✦ Director cheat sheet

| Key | Action |
|---|---|
| `V` | Toggle First-Person WASD Walk mode |
| `W` / `A` / `S` / `D` | Walk / strafe / backward (in Walk mode) |
| `Shift` | Sprint (in Walk mode) |
| `Space` | Jump (in Walk mode) |
| `Shift` + `P` | 📷 Photo (PNG) |
| `Shift` + `T` | Start / stop cinematic tour |
| `Shift` + `R` | Start / stop film recording |
| `Shift` + `H` | Clean mode (hide all UI); `Esc` restores it |
| `F` / `.` | Focus selection (or frame all) |
| `Home` | Frame everything |
| `Esc` | Deselect |

**A good film in 20 seconds:** Looks → *Golden Hour* → Grain on → `Shift+R` → wait → `Shift+R` → your `.webm` downloads.

---

## ✦ Project layout

```
rendra/
├── index.html            the whole studio (engine + Director layer)
├── manifest.webmanifest  install metadata
├── sw.js                 offline cache (stale-while-revalidate, incl. CDN libs)
├── icon.svg / icon-192.png / icon-512.png
└── README.md
```

## ✦ How offline works

1. First visit: the service worker stores the app shell and the CDN libraries (three, openskp, fonts, tailwind).
2. Every later visit: served from cache instantly, refreshed quietly in the background.
3. Bump `V` in `sw.js` to force an update for everyone.

## ✦ Under the hood

The core exposes a tiny bridge, `window.RENDRA = { THREE, scene, renderer, state, controls, … , tick[], post[] }`. The Director layer is built purely on it: `tick` hooks run before each render, and `post` hooks run right after (used for photo capture). You can add your own effects the same way.

## ✦ Notes and limits

- Recording needs a browser with `MediaRecorder` (Chrome, Edge, Firefox, recent Safari).
- Time-of-day covers sunrise to sunset (06:00–18:00). *Blue Hour* uses the twilight end plus lower exposure.
- Very large SKP files depend on your device's memory, because everything happens locally.

---

<div align="center">

*Chalk for the page. Ink for the shadow. Light for everything in between.*

</div>
