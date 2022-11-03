# *Don't:* Radial velocity correction

If your target star is moving towards or away from you, its spectrum will be slightly redshifted or blueshifted. Radial velocity correction removes this redshift or blueshift. This can be useful in some individual studies, but is a banned procedure for AVSpec.

There are two primary forms of radial velocity correction:

### Heliocentric correction

> Heliocentric correction removes the effect of Earth's own motion around the Sun.

### Shifting to rest frame

> Shifting to rest frame removes the radial velocity of the star (in addition to Earth's own motion), so that the wavelengths appear as they would to an observer in a circular orbit around the target star. This generally has the effect of converting the *observed wavelength* to the *emitted wavelength*.

Both operations are banned for spectra uploaded to AVSpec.

## Why not?

1. [Rule #3: Leave analysis to the user](in%20general.md#Leave-analysis-to-the-user). Radial velocity correction is a type of analysis, not a processing step.
2. Radial velocity correction is not required for all science cases, and can be easily applied by the end user.
3. It is best for the end user to have a dataset which is consistent, and we would rather collect uncorrected spectra instead of requiring radial velocity correction for every spectrum.

## Radial velocity correction through calibration

It is possible to apply radial velocity correction (with a low accuracy) by accident, if you use features within your target spectrum to create your calibration. This becomes a noticeable issue above R=1000 ***[[[Check this resolution number]]]***, but some high-velocity targets such as supernovae are vulnerable to this no matter what the resolution is. To learn how to calibrate correctly and avoid accidentially applying radial velocity correction, see [Calibration](../dos/calibration.md).
