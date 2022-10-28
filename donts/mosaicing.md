# *Don't:* Mosaicing

Mosaicing is the process of stitching together multiple pieces of the same spectrum into a panorama. This can be done either at the 2D stage (using photographs) or at the 1D stage (using 1D profiles).

###### IMAGE: Side-by-side comparison of an unmosaiced set of spectra vs. the resulting mosaiced spectrum.

Mosaicing is not allowed for spectra submitted to AVSpec.

## Why not?

1. Mosaicing is unnecessary for almost all science cases, and if an end user does need a mosaic, they can easily create it themselves.
2. Unless you are using an [echelle spectrograph](), each frame in a mosaic is taken at a slightly different time. This can result in confusing and inaccurate results when a spectrum is changing rapidly.
3. It is very easy to accidentally introduce 'seams' when stitching spectra, causing the continuum and/or calibration to suddenly jump or change in slope.

## What should I do instead?

Instead of combining several spectra of the same star into a mosaic, you should **submit each spectrum to AVSpec separately**. That way, the end user has the highest degree of accuracy and flexibility possible.

If you are using an echelle spectrograph, you should use our echelle upload tool.
