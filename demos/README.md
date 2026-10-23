# Runnable prototypes — TANAH

Two single-file demos, extracted verbatim from the specification document in `../docs/`.

| File | Runtime | Open it |
|---|---|---|
| `tanah-composting-instrument.html` | interactive, Tailwind + Lucide CDN | double-click |

The 78-second 3D film now lives in [`../prototype/`](../prototype/) as a Vite project, because it loads Three.js as an ES module and browsers refuse module loads from `file://` origins.


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
