# water_sim

Some stupid shit I am having fun with and am trying to understand some stuff a little better or stuff that just looks cool.


## Live demo

`https://fpfeifle.github.io/water_sim/`.

## Running locally

Just open `index.html` in a browser


## Notes

- Requires WebGL with the `OES_texture_float` extension for the GPU path, falls back to a slower
  CPU 2D-canvas path automatically if unavailable (water sim only).
- Everything (shaders, UI, physics) lives in one HTML file by design, to keep it running with GitHub
