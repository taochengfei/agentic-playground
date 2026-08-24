# cmb — the receding shell

The CMB as the boundary of the observable universe, seen from **outside** — a
god's-eye view. The glowing sphere is the **surface of last scattering**: the
spherical shell where the universe first became transparent, 380,000 years after
the Big Bang. At its center sits **Earth** — us, the observer, the center of
the observable universe; light released on the shell converges there and is
arriving right now.

As "now" (observer cosmic time) advances, the shell grows toward the vantage
point and the pattern on it shifts: the light only now reaching us comes from a
farther comoving region of the shell, revealing what that region looked like
just before it turned transparent.

The space around the shell is not empty: it is pre-recombination plasma, not
yet transparent to us, so it is rendered as the same CMB-like field, dimmed and
desaturated. A quarter (90°) of the shell is cut away so the interior can be
seen directly: near-black space with galaxies in it, with only a faint ghost
of the far side of the CMB shell behind it. The shell is a thin membrane, so
the cut edge keeps a glowing rim of the CMB pattern and nothing extends
toward the center.

Inside the shell, faint galaxy smudges sit at fixed comoving positions — as
the shell grows, more of them come into view.

- Rendering: WebGL1 ray–sphere intersection with a quarter wedge removed and
  an absorbing interior (camera orbits outside the shell, always looking at
  the center) + 2D canvas overlay for galaxies, photons, and a rendered Earth
  at the convergence point. Zero dependencies, no build step.
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
