# Astronomy conventions for data scientists

If you're coming to this course from CS, statistics, or another science, this
page covers the conventions the labs assume. Astronomers reading this: skim it
anyway, you will be explaining these to your groupmates.

## Magnitudes: brightness, but backwards and logarithmic

Astronomers measure brightness in *magnitudes*, a system inherited from
Hipparchus (~150 BC) and formalized so that 5 magnitudes = a factor of 100 in
flux:

    m = -2.5 log10(F) + constant

Two things trip everyone up. **Bigger magnitude = fainter object** (the
brightest stars are ~0, your eye gives out near 6, good telescopes reach 25+).
And magnitudes are logarithmic, so magnitude *differences* are flux *ratios*:
a star 1 mag brighter delivers ~2.5x the flux. Uncertainties quoted in
magnitudes are approximately fractional flux errors (0.01 mag ~ 1%).

*Apparent* magnitude (m) is what you observe; *absolute* magnitude (M) is
what you'd observe from a standard distance of 10 parsecs. The difference is
the *distance modulus*, m - M = 5 log10(d/10 pc), which is how brightness
measurements become distance measurements, the foundation of a surprising
fraction of astrophysics, including the discovery of dark energy.

Why a system built on ratios? Because absolute photometry is hard: what your
detector records is the source times the atmosphere, telescope, camera,
filter, and Galactic dust. Nearly every measurement in practice is a *ratio*
of your target to some calibration source through the same mess, which is
exactly what a magnitude difference is.

## Flux, flux density, and the Jansky

The physical quantity under the magnitudes: *luminosity* L is the power a
source emits (erg/s or W); *flux* F is the power you receive per unit area
(erg/s/cm^2), and F = L / (4 pi d^2). That inverse square is where the
distance modulus comes from. But no detector measures total flux; you measure
flux in a slice of spectrum, i.e. *flux density*, and there are two
conventions: F_nu (per unit frequency, whose natural unit is the *Jansky*,
1 Jy = 1e-26 W/m^2/Hz) and F_lambda (per unit wavelength, typically
erg/s/cm^2/Angstrom). They describe the same spectrum but have different
shapes. The same blackbody peaks at a different place in F_nu than in
F_lambda, and a spectrum that is "flat" in one is not flat in the other. When
a catalog column says "flux," find out which one it is before you fit
anything. The conversion is F_lambda = (c / lambda^2) F_nu, and astropy will
do it for you (see below).

*Surface brightness*, for extended objects like galaxies, is flux per unit
solid angle, usually quoted in mag/arcsec^2, and unlike flux it is
(nearly) distance-independent. Extended objects also make "the" brightness
ambiguous: a quoted galaxy magnitude depends on whether the flux was summed
in an aperture, fit with a model, or integrated to some surface-brightness
cutoff. Two catalogs disagreeing about the same galaxy are often both right.

## Filters and colors

No detector measures "the" brightness; every measurement is through a filter
(a *band* or *passband*) selecting a slice of wavelength. Two systems appear
in this course:

- **Johnson-Cousins / near-IR**: U, B, V, R, I (ultraviolet through
  near-infrared), extended by J, H, K further into the IR. Older, still
  everywhere in the literature. The midterm uses these.
- **SDSS / Rubin**: u, g, r, i, z (plus y for Rubin). Modern surveys
  (SDSS, ZTF, Rubin/LSST) report in these.

The `constant` in the magnitude equation is a *zero point*, and there are two
systems for choosing it. **Vega** magnitudes define the star Vega (or a model
of it) as mag ~0 in every band, the historical choice, and what
Johnson-Cousins UBVRI photometry in the older literature assumes. **AB**
magnitudes define mag 0 as a flat F_nu spectrum at 3631 Jy in every band,
the modern choice, and what SDSS/ZTF/Rubin ugriz(y) photometry uses. The two
systems differ by a band-dependent offset (near zero in V by construction,
growing toward the red to nearly two magnitudes by the K band), so mixing a
UBVRI catalog with an ugriz one without checking is a classic silent bug. Real filters are also not square
cutouts of wavelength: a published passband folds in the telescope, camera,
and detector response, so "the same filter" on two instruments never quite is.

A *color* is a magnitude difference between two bands, written bluer filter
first, e.g. g - r (never r - g). Because magnitudes are backwards, **smaller
color = bluer = hotter** (for stars). Colors are distance-independent, which
is why so many classification methods live in color space.

## Light curves

A *light curve* is brightness vs time, the fundamental data structure of
time-domain astronomy and of half the labs in this course. Conventions:
plotted in magnitudes with the **y-axis inverted** (bright = up); sampling is
usually irregular (weather, moon, telescope schedules), so most classical
signal-processing tools that assume even sampling do not apply, a large part
of why the time-series weeks exist. For periodic sources you will *phase-fold*:
plot brightness against phase = (t mod P)/P for a trial period P.

## Coordinates

Positions on the sky use *right ascension* (RA, the sky's longitude,
often quoted in hours: 24h = 360 deg) and *declination* (Dec, latitude,
in degrees). Catalog matching means finding objects within some angular
tolerance (arcseconds; 1 arcsec = 1/3600 deg) of a position.

## Surveys and acronyms you'll meet

SDSS (Sloan Digital Sky Survey, imaging + spectra, the workhorse of ML
examples), ZTF (Zwicky Transient Facility, time domain), Rubin/LSST (the
NSF-DOE Vera C. Rubin Observatory's Legacy Survey of Space and Time, the
reason this course exists), Kepler/TESS (NASA space photometry, exquisite
light curves), Gaia (ESA astrometry, positions, parallaxes, motions), ASAS
(All Sky Automated Survey, variable stars in several labs).

## Doing this in Python (astropy)

You never need to hand-roll any of the above. `astropy` (already in your
`astr457` conda environment) handles coordinates, units, and time. Every
snippet below runs as-is.

**Coordinates.** `SkyCoord` parses sexagesimal or decimal, converts between
them, computes separations, and transforms frames:

```python
from astropy.coordinates import SkyCoord
from astropy import units as u

c = SkyCoord('05h38m16.9s', '-50d30m50.8s')       # sexagesimal in
c.ra.deg, c.dec.deg                               # (84.5704, -50.5141)

c2 = SkyCoord(84.5704167*u.deg, -50.5141111*u.deg)  # decimal degrees in
c2.to_string('hmsdms')                            # back to sexagesimal

c.separation(c2).arcsec                           # angular separation
c.galactic.l.deg, c.galactic.b.deg                # equatorial -> galactic
```

Catalog cross-matching to within a tolerance is
`SkyCoord.match_to_catalog_sky`. Resist writing your own double loop.

**Units.** Attach units to numbers and let astropy carry them through; it
will refuse to add parsecs to Janskys, which catches real bugs:

```python
(10 * u.pc).to(u.lyr)          # 32.62 lyr
(1 * u.arcsec).to(u.deg)       # 1/3600 deg
```

**Magnitudes and flux.** The AB magnitude system is a unit too, so the
flux-magnitude conversion is one line each way:

```python
(19.5 * u.ABmag).to(u.Jy)      # 5.75e-05 Jy
(3631 * u.Jy).to(u.ABmag)      # ~0 mag (3631 Jy is the AB zero point)
```

F_nu to F_lambda needs to know where in the spectrum you are; that's an
astropy *equivalency*:

```python
(19.5 * u.ABmag).to(u.erg / u.s / u.cm**2 / u.AA,
                    equivalencies=u.spectral_density(550 * u.nm))
# 5.70e-17 erg / (Angstrom s cm2)
```

And the distance modulus really is just a log:

```python
import numpy as np
5 * np.log10(98 / 10)          # 4.96 mag, for d = 98 pc
```

**Time.** Astronomical epochs come as Julian Date (JD) or Modified Julian
Date (MJD = JD - 2400000.5); light-curve time columns are almost always one
of these:

```python
from astropy.time import Time
t = Time('2026-08-25T12:30:00')
t.mjd, t.jd                    # (61277.52, 2461278.02)
```

## To go deeper (all free, all verified)

- Romanishin, *An Introduction to Astronomical Photometry Using CCDs*.
  Read Ch. 1-4 (magnitudes and colors), Ch. 22 (filters), Ch. 25
  (coordinates): <https://www1.phys.vt.edu/~jhs/phys3154/CCDPhotometryBook.pdf>
- SDSS Voyages, "Colors of Objects", ugriz and real catalog numbers,
  hands-on: <https://voyages.sdss.org/launch/launch-into-the-sdss/scavenger-hunt/colors-of-objects/>
- OpenStax *Astronomy 2e* §17.1, the gentlest magnitude introduction:
  <https://openstax.org/books/astronomy-2e/pages/17-1-the-brightness-of-stars>
- Pössel, *A Beginner's Guide to Working with Astronomical Data*
  (arXiv:1905.13189), a course-long companion for FITS files, images, and
  catalogs rather than a first read.
