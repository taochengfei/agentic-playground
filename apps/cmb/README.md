# cmb — the receding shell

The CMB as the boundary of the observable universe. You are at the center; the sky
you see is the **surface of last scattering** — the spherical shell where the
universe first became transparent, 380,000 years after the Big Bang.

As "now" (observer cosmic time) advances, the shell whose light reaches you
*right now* recedes outward and the pattern on it shifts: each line of sight now
corresponds to a farther comoving region, whose 380,000-year-old light is only
arriving today.

- Rendering: WebGL1 inside-out sky (camera at the sphere center) + 2D canvas
  photon overlay. Zero dependencies, no build step.
- The CMB pattern is **synthesized**: random spherical modes with a frequency
  distribution shaped like the acoustic peaks — CMB-like, not the real Planck map.
- The shell distance/time relation (`shellGly`) is a schematic power law, not a
  full ΛCDM integration.

## Controls

| Input | Effect |
|---|---|
| drag | look around the sky |
| slider | set "now" (10.0 → 13.8 Gyr) |
| space | play/pause — the shell recedes as now advances |

## Run

```sh
python3 -m http.server 8000   # from repo root
# → http://localhost:8000/apps/cmb/
```

Also works via `file://`.
