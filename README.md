# Exclusive Inclusion

**Why institutions committed to "inclusion" produce identity-based exclusion.**

A companion site for the paper by Seth C. Oranburg.

- **SSRN:** <https://ssrn.com/abstract=6423378>
- **DOI:** <https://dx.doi.org/10.2139/ssrn.6423378>

---

## Site Structure

| Path | Purpose |
|---|---|
| `index.html` | Landing page |
| `paper/` | Full text of the paper |
| `blog/` | Commentary and short essays |
| `activities/` | Classroom activities and exercises |
| `learning/` | Teaching guides and supplementary readings |
| `inbox/` | Raw source content staging area |
| `visualize/` | Interactive visualization ecosystem |
| `assets/css/` | Shared Oranburg style system |
| `data/` | JSON data files powering all visualizations |

---

## Visualization Ecosystem

Six interactive pages in `visualize/`:

| Page | File | Description |
|---|---|---|
| **ExI Legal Universe Map** *(featured)* | `authority-map.html` | D3.js force-directed graph of the complete legal authority universe — primary cases, secondary authorities, frameworks, reforms, and theoretical anchors. Pan, zoom, filter, search, and find shortest paths between any two nodes. |
| **Disentanglement Matrix** | `matrix.html` | Interactive 2×2 actor/target grid with case studies loaded from `cases.json`. |
| **Immunodeficiency Dashboard** | `dashboard.html` | Governance-void metaphor with arc gauges and faction simulation. |
| **Legal Connectivity Map** | `network.html` | Schematic canvas graph of the five primary cases and three frameworks, loaded from `legal_logic.json`. |
| **Reform Roadmap** | `roadmap.html` | Option-value slider showing why institutions prefer compliance over structural reform. |
| **Intellectual Constellation** | `constellation.html` | Force-directed graph of 2,400 years of governance philosophy surrounding ExI theory. |

### Data files

All visualizations fetch data dynamically from `/data/`:

| File | Contents |
|---|---|
| `manifest.json` | Paper metadata, core thesis, theoretical ancestors |
| `legal_logic.json` | Five primary cases with full holdings, secondary sources, frameworks |
| `reforms.json` | Three structural reforms with mechanisms and procedural safeguards |
| `cases.json` | Five identity-group case studies with empirical data |
| `constellation.json` | Intellectual constellation nodes and edges |

### LawJ integration

The `authority-map.html` page uses a configurable `DATA_BASE_URL` constant at the top of its script block.  When Professor Oranburg's **LawJ** repository becomes available with a richer structured JSON database, update the constant to point to the raw GitHub content URL, e.g.:

```javascript
// In visualize/authority-map.html — top of the <script> block:
const DATA_BASE_URL = 'https://raw.githubusercontent.com/Oranburg/LawJ/main/data/';
```

All other visualizations that fetch from `../data/` can be updated similarly to pull from LawJ automatically. The data schema used internally (nodes with `id`, `label`, `detail.tabs`, `detail.connections`) is forward-compatible with richer data sources.

---

## Style

This site uses the shared **Oranburg style system** (`assets/css/oranburg-style.css`), the canonical design foundation across Professor Oranburg's academic sites. It features:

- **Dark mode default** with light mode toggle (persisted in `localStorage` as `ei-theme`)
- **Color palette:** deep navy (`#0A3255`), crimson red (`#B21F2C`), sky blue (`#6DACDE`), gold (`#FFD65C`), teal (`#B5E1E1`)
- **Typography:** Oswald (headlines), Crimson Text (body/accent), Roboto (UI), Roboto Mono (code)
- **Responsive** mobile-first layout

---

## Adding Content

Drop raw files into the `inbox/` directory. See [`inbox/README.md`](inbox/README.md) for workflow details.

To add new authority nodes to the Legal Universe Map, update the relevant JSON file in `data/` — the visualization will pick up the new data automatically on the next page load.

## License

© 2026 Seth C. Oranburg. All rights reserved.
