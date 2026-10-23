# TANAH — decentralised neighbourhood food-waste composting

**Thesis:** a township pays twice for the same material. Once to haul food waste to a landfill, and again to buy compost and soil hauled back in through the same gate. TANAH asks a narrow question: if the waste is composted within 200 m of the beds that need it, what does a diverted tonne actually cost?

The answer is reported even when it is unflattering. The 12-week pilot model in the instrument comes out at **RM 399.71 per diverted tonne** against a RM 43/t Selangor landfill tipping fee and a RM 216/t industrial composting benchmark — a **FAIL**. That number is the point: fixed tooling spread over a small pilot volume dominates unit economics, and hiding it only moves the discovery to Q&A.

---

## Runnable prototypes

| File | What it does | Needs |
|---|---|---|
| [`demos/tanah-3d-workflow.html`](demos/tanah-3d-workflow.html) | The 78-second 3D film across three chapters: **before** (household bin → municipal compactor → landfill, plus purchased compost arriving separately), **the intervention** (5 L caddies → 200 m transfer → weighing → contamination removal → carbon layering → four-stage maturation), **after** (wheelbarrow to adjacent beds, root-zone application, closed local loop while the landfill route fades). Play/pause/replay and chapter skip. | Internet (Three.js 0.160 ES module) **and a local server** |
| [`demos/tanah-composting-instrument.html`](demos/tanah-composting-instrument.html) | The pilot instrument: weigh-in ledger, cash-flow model, steady-state scale simulator (200 → 20,000 households, paid vs. volunteer labour), treated-vs-control landscape plots, 12-week participation audit, and an 8-step guided pitch mode. | Internet (Tailwind, Lucide, Google Fonts) |

### Running them

`tanah-composting-instrument.html` opens by double-click. `tanah-3d-workflow.html` loads Three.js as an ES module, which browsers block on `file://` origins — serve the folder:

```bash
cd demos
python -m http.server 8000
# then open http://localhost:8000/tanah-3d-workflow.html
```

## Specification

| File | What it covers |
|---|---|
| [`docs/TANAH_3D_Workflow_Demonstration_Source_Package.docx`](docs/TANAH_3D_Workflow_Demonstration_Source_Package.docx) | Complete runnable source: procedural asset builders, animated workflow actors, camera interpolation, renderer/scene setup, and the scene-by-scene timeline that the HTML prototype implements. |

## What is measured, modelled and assumed

- **Measured (field, in the real pilot design):** gross and net bucket weights, contamination weight, pile temperature, surviving shrub counts in treated and control beds.
- **Assumed:** household generation of 1.17 kg/person/day with a 30.6% food share, 4-person households, 55% participation, 25% compost yield.
- **Benchmarks:** RM 43/t Selangor landfill tipping fee, RM 216/t industrial composting.
- **Illustrative:** the seeded weigh-in (`157.5 kg in`, `12.6 kg contamination`, collector name). The app ships with a **Field Mode** toggle that clears it, so a demo can never be mistaken for a record.

The instrument contains no simulated IoT telemetry and does not claim net developer savings under paid labour — the steady-state model shows that only volunteered labour brings the unit cost below the landfill fee.

## Status

- Specification: complete as a document.
- Prototypes: runnable from `demos/`.
- No completed field pilot, no deployed sensors, no production backend.
