# Y-axis rescaling

Y-axis rescaling is the process of multiplying or dividing the entire spectrum by a **single constant**, causing the units on the y-axis to change *without* changing anything else about the spectrum.

This is similar to flux calibration, but without any physical motivation (i.e. the resulting y-axis units don't represent a physical quantity).

## Is it allowed?

Since y-axis rescaling does not alter the shape of the spectrum at all, and the y-axis units are virtually always arbitrary anyway, spectra which have undergone this procedure are perfectly acceptable for AVSpec.

## Why do it?

Some people choose to rescale their spectra so that a wavelength near the center has a y-axis value of 1. This can make it easier to read values on the y-axis, or to plot several spectra on the same graph, but is not in any way necessary for science.

###### IMAGE: Side-by-side example. Left side: two spectra with raw y-axes that don't fit together well in the same plot. Right side: the same spectra with rescaled y-axes.

The AAVSO neither recommends nor forbids y-axis rescaling of spectra submitted to AVSpec.

## Confusion with the term "normalization"

In some papers, y-axis rescaling is referred to as "normalization". However, AVSpec exclusively uses the term "normalization" to refer to "continuum rectification", a different and destructive operation; see [Normalization](../donts/normalization.md).
