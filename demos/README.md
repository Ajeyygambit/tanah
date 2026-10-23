# Runnable prototypes — TANAH

Two single-file demos, extracted verbatim from the specification document in `../docs/`.

| File | Runtime | Open it |
|---|---|---|
| `tanah-3d-workflow.html` | 78 s auto-play, Three.js 0.160 ES module (jsdelivr) | **local server required** |
| `tanah-composting-instrument.html` | interactive, Tailwind + Lucide CDN | double-click |

```bash
cd demos
python -m http.server 8000
# http://localhost:8000/tanah-3d-workflow.html
```

The ES-module import is why the first one needs a server; browsers refuse module loads from `file://` origins.

## `tanah-3d-workflow.html`

Three chapters, ten scenes, 01:18 total, with play/pause/replay and chapter skip:

1. **Before (0:00–0:25)** — food scraps into the general bin, municipal compactor to the landfill, tilt-and-unload, and a *second* truck arriving with purchased compost through the same gate.
2. **The intervention (0:25–0:48)** — 5 L caddies, sub-200 m transfer, manual weighing, plastic contaminant picked out into the reject bin, dry leaves as carbon source, four-stage maturation time-lapse in a three-bay timber station.
3. **After (0:48–1:18)** — wheelbarrow to the adjacent bed, compost worked into root-zone soil (not foliage), wide loop reveal across neighbourhood nodes while the landfill route fades, then the before/after comparison frame.

Every numeric callout is prefixed **ILLUSTRATIVE** — the weigh-in reads `≈ 14.2 kg` and is never presented as a sensor feed.

## `tanah-composting-instrument.html`

The pilot instrument, eight tabs:

- **Live board** — headline cost per diverted tonne with a three-way verdict against RM 43/t landfill and RM 216/t industrial composting; before / after / compare.
- **Weigh-in** — log a bucket drop; net diverted recalculates the whole model.
- **Costs** — labour, tooling, water, supervision, with a volume-distortion warning that states plainly how much each RM 100 of fixed cost adds per tonne at pilot volume.
- **Scale** — 200 → 20,000 households, and a paid/volunteer labour switch that flips the verdict.
- **Plots** — treated vs. control bed survival and replacement cost.
- **Participation** — 12-week decay and contamination tracker.
- **Methodology** — every formula with the numbers substituted.
- **Pitch mode** — eight guided steps, opening with the losing number.

Demo data is seeded and labelled. **Field Mode** clears the ledger so only genuine entries remain.
