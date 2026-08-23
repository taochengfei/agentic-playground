# cmb — the receding shell

The CMB as the boundary of the observable universe, seen from **outside** — a
god's-eye view. The glowing sphere is the **surface of last scattering**: the
spherical shell where the universe first became transparent, 380,000 years after
the Big Bang. The point at its center is the observer (us); light released on
the shell converges on that point and is arriving right now.

As "now" (observer cosmic time) advances, the shell grows toward the vantage
point and the pattern on it shifts: the light only now reaching us comes from a
farther comoving region of the shell, revealing what that region looked like
just before it turned transparent.

The space around the shell is not empty: it is pre-recombination plasma, not
yet transparent to us, so it is rendered as the same CMB-like field, dimmed and
desaturated. Inside the shell, faint galaxy smudges sit at fixed comoving
positions — as the shell grows, more of them come into view.

- Rendering: WebGL1 ray–sphere intersection (camera orbits outside the shell,
  always looking at the center) + 2D canvas overlay for galaxies and photons.
  Zero dependencies, no build step.
- The CMB pattern is **synthesized**: random spherical modes with a frequency
  distribution shaped like the acoustic peaks — CMB-like, not the real Planck map.
- The shell distance/time relation (`shellGly`) is a schematic power law, not a
  full ΛCDM integration.

## Controls

| Input | Effect |
|---|---|
| drag | orbit the view around the shell |
| slider | set "now" (0.0 → 13.8 Gyr) |
| space | play/pause — the shell grows as now advances |

## Run

```sh
python3 -m http.server 8000   # from repo root
# → http://localhost:8000/apps/cmb/
```

Also works via `file://`.
