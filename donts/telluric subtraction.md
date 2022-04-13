# *Don't:* Telluric subtraction

Some software packages for astronomical spectroscopy make it possible to subtract [telluric absorption lines](../reference%20spectra/tellurics.md) from your finished spectra. This can be useful for performing analyses on your own. However, **you should not submit spectra with altered telluric lines to AVSpec.**

## Why not?

AVSpec's validation of submitted spectra relies on the presence of telluric absorption lines, so that we can check the [calibration](../corrections%20for%20scientifically%20valid%20spectra/calibration.md) independently of radial velocity.[^1] Though it is not always possible to use telluric lines since they do not exist at all wavelengths, handling spectra which are missing telluric lines makes the validators' jobs harder, and validation will proceed faster if tellurics are available.

## Telluric subtraction through overfitting

Sometimes, overfitting during IR correction can reduce the depth of telluric bands, or even eliminate them entirely.

###### IMAGE: Example of a spectrum with oversubtracted tellurics vs. a good spectrum

This is a warning sign for serious issues with the validity of the spectrum, and the overfitting should be fixed before submitting spectra to AVSpec. See [overfitting](overfitting.md) for more information.

[^1]: Spectra should not be corrected for radial velocity; see: [Don't: Radial velocity correction](radial%20velocity%20correction.md)