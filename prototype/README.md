# TANAH — 3D physical workflow demonstration

A 78-second, three-chapter 3D film of the TANAH workflow, as a single self-contained page.

## Quick start

### Option A — zero build

`index.html` loads Three.js from a CDN as an ES module. Browsers block module imports from `file://`, so serve the folder:

```bash
npx serve .
```

### Option B — bundled offline build (recommended on stage)

`npm install` pulls Three.js into the project, so nothing is fetched during the pitch.

```bash
npm install
npm run dev        # full-screen presentation server
npm run build      # static bundle in dist/
npm run preview    # serve the built bundle on :4173
```

## Controls

- **Automatic playback** — 00:00 to 01:18 across three chapters, then stops on the final frame.
- **PLAY / PAUSE** — freeze any keyframe during Q&A.
- **REPLAY** — restart at 00:00.
- **Chapter skip** — `1. BEFORE TANAH` (00:00), `2. TANAH INTERVENTION` (00:25), `3. AFTER TANAH` (00:48).
- **Timeline scrubber** — click anywhere on the progress bar.

## What the film shows

| Chapter | Time | Content |
|---|---|---|
| Before | 0:00–0:25 | Food scraps into the general bin; municipal compactor to the landfill; tilt-and-unload; a second truck arriving with purchased compost through the same gate. |
| Intervention | 0:25–0:48 | 5 L caddies; sub-200 m transfer; manual weighing; plastic contaminant removed to the reject bin; dry leaves as carbon source; four-stage maturation time-lapse. |
| After | 0:48–1:18 | Wheelbarrow to the adjacent bed; compost worked into root-zone soil, not foliage; wide loop reveal as the landfill route fades; before/after comparison frame. |

## Provenance

Every numeric callout is prefixed **ILLUSTRATIVE**. The weigh-in reads `≈ 14.2 kg` and is never presented as a sensor feed. Benchmarks quoted (RM 43/t landfill, RM 216/t industrial composting, 1.17 kg/person/day, 30.6% food share, 25% yield) are context, not measurements from this animation.

Township geometry is procedural and does not depict an identifiable real development. No developer, government or certification body endorsement is implied.
