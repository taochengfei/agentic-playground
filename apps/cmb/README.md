# cmb — the receding shell, the plasma, and the timeline

Three stacked full-height scenes; scroll down to move between them (the page
snaps softly, scrollbars stay usable).

**I · The shell.** The CMB as the boundary of the observable universe, seen
from **outside** — a god's-eye view. The glowing sphere is the **surface of
last scattering**: the spherical shell where the universe first became
transparent, 380,000 years after the Big Bang. At its center sits **Earth** —
us, the observer; light released on the shell converges there and is arriving
right now. As "now" (observer cosmic time) advances, the shell grows toward
the vantage point and the pattern on it shifts. The space around the shell is
pre-recombination plasma, not yet transparent, so it is rendered as the same
CMB-like field, dimmed; a quarter (90°) wedge is cut away so the interior —
near-black space with faint galaxy smudges at fixed comoving positions — can
be seen directly.

**II · The plasma.** A particle encoding of the physics inside that fog,
viewed top-down as a slab of photon-baryon gas. Free electrons scatter light
every few centimeters, so photons cannot cross the universe in a straight
line — the bright curls are photon paths: straight legs between scatterings,
direction re-rolled at every event, with a slow flow field biasing them. The
faint expanding rings are sound: acoustic oscillations racing through the gas
(gravity compresses, radiation pressure pushes out). Gas dots brighten where
a compression band passes; the same ripples, frozen at recombination, are the
hot and cold spots of scene I. Click the fog to stir your own ripple.

**III · The timeline.** One 30-second looping march from 1 second to today on
a logarithmic time axis, each era with its own visual regime: an opaque,
fast-churning **fire** (no atoms yet) → a **fog** that thins, where acoustic
rings appear and, at recombination (380,000 years), released light starts
streaming straight and fast → **transparent space**: sparse cold stars,
galaxies, a faint echo of the shell rim, and the CMB arriving now —
converging on Earth at the center. Scrub the slider to inspect any moment.

## Controls

| Input | Effect |
|---|---|
| scroll | move between the three scenes |
| drag | orbit the shell (scene I); touch drags scroll vertically |
| slider (I) | set "now" (0.0 → 13.8 Gyr); pauses the march |
| slider (III) | scrub cosmic time (1 s → 13.8 Gyr, log); pauses the march |
| space | play/pause the visible scene |
| click (II) | stir a ripple in the fog |

## Notes

- Rendering: WebGL1 ray–sphere intersection with a quarter wedge removed and
  an absorbing interior (scene I) + 2D canvas particle layers (scenes II/III).
  Zero dependencies, no build step; all sprites are generated at load.
- Only the scene(s) currently on screen animate (IntersectionObserver gating)
  so a scroll-resting page costs no frames.
- The CMB pattern is **synthesized**: random spherical modes with a frequency
  distribution shaped like the acoustic peaks — CMB-like, not the real Planck map.
- The shell distance/time relation (`shellGly`) and the timeline's log scale
  are schematic, not a full ΛCDM integration.
- The app now runs ~950 lines across the three scenes, beyond the ~500-line
  guideline — kept in one file and zero-dependency anyway; split under
  `apps/cmb/` if a fourth scene ever lands.

## Run

```sh
python3 -m http.server 8000   # from repo root
# → http://localhost:8000/apps/cmb/
```

Also works via `file://`.
