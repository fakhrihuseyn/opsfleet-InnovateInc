<img src="image.png" alt="alt text" style="max-width:480px; width:10%; height:auto; display:block; margin:12px 0;" /> 

# Opsfleet-InnovateInc

Innovate Inc. - Web Application Platform

## Viewer & Layout

This repository includes a small static HTML viewer that renders the architecture diagrams found in the `.infra/` folder.

- The viewer renderer is an `index.html` 
- Layout and visual presets are defined per-diagram in the viewer (`index.html`) under `diagramConfigs` (CICD, EKS, High Level, Network). Colors and toolbar styles are centralized in `style.css`.
- The full architecture rationale and design choices are documented in [ARCHITECTURE_DESIGN.md](ARCHITECTURE_DESIGN.md).

Viewer features:

- Toolbar with diagram selector, search, scale control, Fit and zoom buttons.
- Icon assets are served from `assets/icons/`. The viewer will fall back from `.svg` to `.png` when an SVG path fails to load.
- Hover tooltips on icons, hover enlargement, and click-to-center with a mild zoom.
- Per-diagram presets are available in the viewer for visual tuning (see `diagramConfigs` inside `index.html`).

Run locally
1. Download repository to your local

2. Start a simple static server in the repository root:

```bash
python3 -m http.server 8000
```

3. Open [http://localhost:8000](http://localhost:8000) in your browser and choose a diagram from the toolbar.


