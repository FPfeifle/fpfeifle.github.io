# water_sim

An interactive, single-file, GPU-accelerated physics & astrophysics simulator that runs entirely
in the browser — no build step, no dependencies, just a static HTML file. Originally a water-wave
and lighting sandbox, it now covers seven phenomena selectable from one dropdown:

- **Water Sim** — 2D wave equation on a GPU-simulated height field, draggable point/line/circle
  light sources, adjustable color temperature, wall/emitter drawing, reflective or absorbing edges.
- **AGN Jet — Spine/Sheath** — relativistic jet structure, viewing-angle-dependent Doppler boosting,
  and a particle-interaction view (synchrotron, inverse-Compton, etc.).
- **Stellar Evolution — HR Diagram** — main-sequence and post-main-sequence evolutionary tracks.
- **Galaxy Rotation Curve** — visible vs. dark-matter-implied rotation curves.
- **Blazar Spectral Energy Distribution** — the characteristic double-humped SED.
- **Pulsar P–Ṗ Diagram** — period vs. period-derivative, spin-down age, magnetic field tracks.
- **IACT Gamma-Ray Air Shower** — simulates a shower striking the atmosphere and flashes the
  resulting Cherenkov image onto one or two telescopes. With two telescopes it does genuine
  stereoscopic reconstruction: both camera images are plotted in one shared frame and the
  intersection of their major axes gives the reconstructed direction.

## Live demo

Hosted via GitHub Pages at whatever this repo's Pages URL is (Settings → Pages), e.g.
`https://<username>.github.io/water_sim/`.

## Running locally

No build step — just open `index.html` in a browser, or serve the folder locally:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Files

- `index.html` — the simulator (this is what GitHub Pages serves at the repo root).
- `water_sim_webgl.html` — identical copy, kept so existing links to this filename still work.

## Notes

- Requires WebGL with the `OES_texture_float` extension for the GPU path; falls back to a slower
  CPU 2D-canvas path automatically if unavailable (water sim only).
- Everything (shaders, UI, physics) lives in one HTML file by design, to keep it a drop-in
  GitHub Pages / Codepen-style artifact.
