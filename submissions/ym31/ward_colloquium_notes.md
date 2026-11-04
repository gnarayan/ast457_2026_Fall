# Colloquium Notes 9/22 (Charlotte Ward)

- Talk was about combining Rubin, Euclid and Roman. Rubin = deep ground based optical, Euclid = space so way higher resolution + IR, Roman just launched
- Problem is Rubin is "too good", so deep that a lot of galaxies overlap (30-60%?). messes up shapes for weak lensing, photo-z's, photometry
- Use Euclids sharp images to figure out how many sources there are and their shapes, then use that for the Rubin photometry
- easy version is take Euclid shapes and force photometry on Rubin. Harder version (DDP3?) models the sky once and renders it to look like each telescope's image, fits everything together
- with space images galaxies have spiral arms etc so simple profiles don't work, every pixel becomes a parameter -> really degenerate, so they need ML priors and GPUs
- Their code is Scarlet 2, its written in JAX (GPU)
- Scarlet 2 has a diffusion model prior that pushes it toward realistic galaxy shapes when the data doesn't constrain it
- can also fit single exposures for transients so you dont need a template
- Lensed supernovae, Rubin will find a bunch, time delays give the Hubble constnat. Someone in her group showed you can get time delays from Rubin alone even when the images are blurry
- Wandering black holes: in small galaxies the BH might not be in the center. They found a TDE offset from the center of its galaxy in ZTF, HST confirmed. Probably a ~10^6 Msun BH from a minor merger
- changing look AGN, idea is disk tearing from GRMHD sims makes the variability faster than normal
- radio stuff with ASKAP, some AGN got radio loud but most werent related to the changing look ones

## Questions

1. If Scarlet 2 fits every single exposure without a template, isn't that way slower than difference imaging? Could it run on all of LSST?
2. For the offset TDE how do they know it's a wandering black hole and not just in a small galaxy that's too faint to see?
