# Colloquium notes: Kareem El-Badry, "Black Holes and Revelations: Unseen Companions in Stellar Binaries"

**Astronomy Colloquium, Sep 8, 2026 (Caltech).** Watched the YouTube recording
(https://www.youtube.com/watch?v=sYhMdMLzVno). Notes by Yiming Ma (ym31).

## 1. The framing: where are the Milky Way's ~10^8 black holes?

- Opens with Zeta Oph, the nearest O star (~100 pc, >20 Msun, ~5 Myr lifetime).
  There are ~20,000 O stars in the Galaxy today. Multiply by (age of Galaxy /
  O-star lifetime) = 10 Gyr / 5 Myr ~ 2000, so a few x 10^7 O stars have ever
  lived and of order 10^8 stellar-mass BHs should exist in the Milky Way. He was
  careful to flag the sloppiness: constant SFR assumed, not every O star makes a
  BH, some BHs come from lower-mass stars.
- Neat scaling argument: ~1000 BHs per O star, and a factor of 1000 in volume
  is a factor of 10 in distance, so the nearest BH should be ~10 pc away.
- What we actually have:
  - ~20-25 dynamically confirmed BH X-ray binaries (mass function from the
    companion's RV curve + companion mass estimate; >3 Msun and a bright X-ray
    source => BH). ~50 more are "probable" from X-ray properties only.
  - New transients keep appearing (~1/yr) but dynamical confirmations flattened
    after ~2000 because the new ones are too faint to follow up.
  - Gravitational-wave BBHs: many with components >30 Msun, i.e. more massive
    than anything in the local X-ray binary sample. So no local analogs of the
    LIGO population, and we can never get a progenitor metallicity for a GW
    source.
  - Neutron stars with good masses: a few dozen, mostly recycled radio pulsars.
- The "stellar graveyard" plot shows the apparent bimodality: NSs mostly <2 Msun,
  BHs mostly >5 Msun, few objects in between. He was explicit that this could be
  supernova physics OR a selection effect from how each population is found.
- Open questions listed: underlying BH/NS mass distribution; dependence on
  progenitor mass, metallicity, rotation; natal kicks; how BH binaries form and
  survive; and "what else is out there" (BH+BH orbited by a star, unusually
  low/high mass BHs).

## 2. Gaia as a binary machine

- Gaia sat at L2 for 11 years (2014-2025, now retired), scanning the whole sky
  ~monthly, ~100 astrometric epochs per source. Bright-end precision ~0.01 mas.
  His analogy: the width of a human hair seen from California to Indiana (on a
  flat Earth). Also: 0.01 mas is ~1/10 of the size of the EHT M87 image, though
  Gaia can only centroid to that precision, not resolve.
- A full astrometric orbit has 12 free parameters (Keplerian elements + parallax
  + proper motion), so ~100 epochs gives ~10x more data than parameters.
- DR3 (2022) used only the first ~3 years (~1000 day baseline) and delivered
  ~170,000 astrometric binary orbits, vs. 235 from Hipparcos. Dip in the period
  distribution at exactly 1 yr because parallax and orbital motion become
  degenerate there. Most hosts are Sun-like stars (sensitivity, not physics).
- Follow-up bookkeeping from his group: ~5000 WD+MS candidates (~90% confirmed),
  ~50 NS+MS candidates (~30 confirmed), 5 BH candidates (2 confirmed). His
  explanation for the very different confirmation rates: a roughly constant
  background of bad orbits, so rarer populations are more swamped by false
  positives. That is the same logic as a low base rate driving down precision.
- DR4 is scheduled for **Dec 2, 2026**: doubles the baseline to ~2000 days,
  which by Kepler's third law means physically larger orbits are characterizable,
  which Gaia can resolve to larger distances, so ~10x the survey volume for
  binaries. Also the DR3 quality cuts on which orbits got published will be
  relaxed. "Even though we stopped taking data, the best is yet to come."

## 3. The three Gaia black holes

| System | Star | BH mass | Period / separation | Metallicity | Distance |
|---|---|---|---|---|---|
| Gaia BH1 | ~0.9 Msun, Sun-like | 9.3 Msun | ~0.5 yr, ~1.4 AU, e~0.45 | ~solar | ~0.5 kpc |
| Gaia BH2 | ~1 Msun, subgiant | ~9 Msun | ~3.5 yr, ~5 AU, eccentric | ~solar | ~1.2 kpc |
| Gaia BH3 | low-mass, halo | 33 Msun | longer, e~0.7 | [Fe/H] = -2.5 | pre-DR4 early release |

- Method: Gaia gives the 2D sky-plane ellipse + parallax; ground-based RVs give
  the line-of-sight component; combined 3D orbit + luminous star mass =>
  companion mass. The companion is dark, so it has to be a BH.
- **Formation problem for BH1/BH2:** a ~40 Msun progenitor becomes a red
  supergiant with R ~ 5-10 AU, which would engulf a star at ~1 AU. Common
  envelope is the default answer but the orbital energy released scales as
  1/(final separation), so spiraling in only to ~1 AU liberates far too little
  to eject the envelope. That works for X-ray binaries (tight final orbits) but
  not for these wide systems. He joked there are more models than Gaia BHs.
  Families of solutions: (a) progenitor never expands and goes straight to a WR
  star, but then mass loss widens the orbit so the star had to start at ~0.1 AU;
  (b) started as a triple with an inner massive binary that stopped each other
  from expanding; (c) dynamical exchange in a cluster, so the binary never had
  to survive the stellar evolution.
- The eccentricities (0.4, 0.5, 0.7) are consistent with dynamical formation but
  not evidence against binary evolution, since massive binaries are often
  eccentric and a natal kick would make a circular orbit eccentric anyway.
- BH3 is in the ED-2 stellar stream, a dissolving ~10^4 Msun cluster. Over
  10 Gyr in such a cluster, exchange encounters are hard to avoid, so for BH3
  specifically dynamical origin (or at least post-formation exchanges) is likely.
- A big advantage over GW sources: the luminous companion's spectrum gives the
  progenitor's metallicity, whether the pair formed as a binary or in a cluster.
  Two solar-metallicity ~9 Msun BHs and one [Fe/H] = -2.5 33 Msun BH: the
  tempting story is metal-poor stars have weaker winds, so more mass survives to
  collapse. He drew the line through three points and immediately said it needs
  more points.
- **Is it one BH or two?** Student Pranav Nagarajan tested BH1 with ~40 x 15 min
  ESPRESSO/VLT RVs (~10 hr total). A star orbiting an inner BH+BH binary sees a
  non-Keplerian potential: a short-period wobble at half the inner period plus a
  slow precession of the outer orbit. Residuals look like pure noise, mass
  function measured to ~4 significant figures. Simulations of star+BBH triples
  rule out inner periods > 1.5 days; anything shorter would merge in a few Gyr
  (less than the system age), so a surviving inner binary would require fine
  tuning. Conclusion: single BH. He called this realistically the only way to
  find a Milky Way analog of a LIGO binary.
- Period-distance census: X-ray binaries at short periods, Gaia BHs at long
  periods (Gaia needs a big ellipse on the sky). The three Gaia BHs are the
  three nearest known BHs, so wide non-accreting BH binaries are probably
  intrinsically more common than X-ray binaries; they were just invisible before
  Gaia. Also one isolated BH from microlensing.

## 4. Gaia neutron stars

- ~20+ (now 27) dark companions at 1.3-2 Msun on eccentric orbits around
  main-sequence stars. Main alternative to a NS is a close double white dwarf;
  he could not construct a binary-evolution path to that configuration but
  explicitly left it open ("the universe is more creative than we are").
- Mass uncertainties are only a few percent, so this is close to a pristine
  natal NS mass distribution: it has real width, and the most massive one
  (~1.9 Msun) cannot have accreted from its MS companion. So NSs are not born
  at a single mass.
- Sensitivity argument for the mass gap: a 5 Msun companion would be far easier
  to detect than a 1.4 Msun one, yet many NSs and no 2-5 Msun objects are seen.
  So if low-mass BHs exist in these binaries, they are much rarer than NSs. The
  bimodality persists over ~4 orders of magnitude in orbital period across the
  Gaia, X-ray, and radio-pulsar samples.
- **Lithium puzzle:** all the metal-poor NS companions are strongly Li-enhanced
  relative to matched field stars. Li enhancement is known in X-ray binary
  donors, but those explanations rely on proximity to the compact object and
  these companions are AU-scale away. He openly asked the audience for ideas.
- Future evolution (MESA models by Pranav): when the companion evolves up the
  giant branch and fills its Roche lobe it becomes a symbiotic X-ray binary like
  IGR J16194-2810 (red giant + NS, 2.1 kpc). X-ray bright phase lasts only a few
  Myr vs. a few Gyr X-ray faint, so ~1000 faint systems per bright one; rates are
  consistent with the Gaia NSs being the progenitors of the symbiotic XRBs.

## 5. Kicks: strong and weak

- Space velocities of BH X-ray binaries + Gaia BHs vs. matched disk-star
  populations: more systems in the outskirts of the velocity distribution than
  random sampling allows. Some BHs need kicks of >100 km/s.
- Counterexample: V404 Cyg (one of the best-studied BH XRBs) has a tertiary at
  ~5000 AU with identical proper motion, parallax, and RV (work with Kevin
  Burdge). The outer orbit's escape speed is ~2 km/s, so the BH must have been
  born with a kick of at most a few km/s. Different formation modes give
  different kicks.
- The tertiary may have built the system: start with a wide (~100 AU) inner
  binary that never has a red supergiant interaction, then von Zeipel-Lidov-Kozai
  oscillations drive the inner eccentricity to ~0.999, tidal dissipation at
  periastron shrinks the orbit, and you get an LMXB. Population models of BH
  triples produce exactly this kind of inner/outer configuration.

## 6. What comes next

- DR4 simulations: with a log-uniform period distribution normalized to the two
  DR3 detections, expect many more low-mass star + BH systems, especially at
  P > 1000 d. A separate model (Langer et al. 2020 binary evolution coupled to a
  luminous-star catalog) predicts ~50 massive star + BH binaries in DR4; he
  thinks that is optimistic but expects at least a handful. Massive-star
  companions matter because those can eventually become GW sources.
- Astrometric orbits can be wrong, and even correct orbits can be misread
  (a "dark" companion that is really a fainter luminous star). Plan:
  multi-epoch spectra, high-resolution imaging, high-energy follow-up. Because
  the periods are years, the RV follow-up will take years. Expect a candidate
  catalog soon after DR4, then a long confirmation tail.
- Roman (recently launched, headed to L2): the Galactic Bulge Time Domain
  Survey will find isolated BHs via microlensing, and its space-based astrometry
  breaks the mass / proper-motion degeneracy of a photometric light curve alone.
  A single later Roman or Euclid epoch can collapse the uncertainty on a long
  Gaia orbit that the DR3 baseline alone cannot close.
- Closing point: most open questions in stellar physics come back to binary
  evolution, and we still lack good models for how the BHs we can actually
  study (XRBs and these wide systems) formed.

## 7. Q&A highlights

- Could ESPRESSO-level RVs detect a hot Jupiter around a Gaia BH companion?
  Yes in principle; that was in the proposal, though at 14th mag the error bars
  would not catch every case.
- DR4 sensitivity to massive-star binaries: astrometry does not care what the
  companion is; DR3 was limited by the publication cuts, and DR4 should give
  direct astrometric masses for many massive stars, often needing spectra or
  imaging to pin down flux ratios.
- Stuart Shapiro (remote) asked how the 1.3 Msun "neutron stars" are
  distinguished from cold or rotating massive white dwarfs. Answer: for any one
  object you cannot be sure; the 1.3 Msun cut is where the eccentricity
  distribution changes (WD companions are mostly circular, these are e ~ 0.5).
  ~20 of the 27 are above 1.4 Msun, so not all can be WDs. Rotational support
  cannot be ruled out directly but is unlikely to persist for Gyr.
- On BH3 being very old: mainly it means lots of time for dynamical encounters.
- On the LIGO mass spectrum: the GW distribution is sharply peaked near
  9 Msun (roughly 9 of 10 draws land at 8-11 Msun), with another feature near
  30 Msun, matching BH1/BH2 and BH3 suspiciously well. His take: if you had to
  bet on a BH mass, 9 Msun is a good bet.

## 8. My two questions

1. **Kicks vs. mass.** The population argument says some BHs need kicks
   >100 km/s, while V404 Cyg's tertiary requires <5 km/s. Is there a trend of
   kick velocity with BH mass in the current sample (as fallback-dominated
   collapse would predict, with the most massive BHs getting the weakest kicks)?
   In particular, does Gaia BH3 at 33 Msun have a space velocity consistent with
   the ED-2 stream to within a few km/s, and would that constrain its kick the
   same way the V404 Cyg tertiary does? I could not tell from the talk whether
   the kick analysis is done separately for the Gaia BHs versus the XRBs, and
   whether the XRBs' high velocities could partly come from the mass transfer
   history rather than the natal kick.

2. **Selection effects and the DR3 to DR4 forecast.** The DR4 yield is
   normalized to two DR3 detections assuming a log-uniform period distribution.
   How sensitive is the "~10x" forecast to that assumption, and to Gaia's
   detection efficiency as a function of eccentricity? All three Gaia BHs are
   eccentric (e = 0.45-0.7). Is that because BH binaries really are eccentric,
   or because an eccentric orbit produces a larger or more distinctive
   astrometric signal at fixed period so DR3's quality cuts preferentially kept
   them? If the latter, the "eccentricities favor dynamical formation" argument
   and the DR4 yield prediction both need the selection function folded in.
   This is essentially the same completeness / base-rate issue as the WD vs NS
   vs BH confirmation rates he described.

*(A smaller one, more for myself: for the Li-rich NS companions, could cosmic
ray spallation in the supernova ejecta hitting the companion make Li at AU
separations, and would that predict a correlation between Li abundance and
separation or eccentricity across the 27 systems?)*
