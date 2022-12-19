# AVSpec data reduction guidelines

On this page, you'll find AVSpec's official guidelines for processing spectra. If you follow all of the procedures listed in the *Required* section, your spectra can be accepted into AVSpec.

If you are an observer, please also read [Three Rules for Quality Spectra](three%20rules%20for%20quality%20spectra.md).

## Required

These procedures **must** be performed on every spectrum submitted to AVSpec.

- [Wavelength calibration](dos/calibration.md)
- [Background subtraction](dos/background%20subtraction.md)
- [Contaminant trimming](dos/contaminant%20trimming.md)
- [Flat field correction](dos/flats.md) *(slit spectrographs only)*
- Pseudoflat correction - camera sensor pixel-to-pixel variations only *(slitless only)*
- [Dark frame correction](dos/darks.md)

## Recommended

The AAVSO recommends that you perform these procedures on every spectrum you submit to AVSpec. Doing so will allow your spectrum to be marked as 'Recommended' within the database.

- [Instrument response correction](dos/instrument%20response%20correction.md)
- [Stacking](dos/stacking.md)
- Dithering *(slitless only)*

## Allowed

These procedures are considered neutral; they may be performed on spectra submitted to AVSpec, but are not specifically recommended by the AAVSO.

- [Binning](allowed/binning.md)
- [Rescaling the y-axis](allowed/y-axis%20rescaling.md)
- [Flux calibration](allowed/flux%20calibration.md)

## Banned

If a procedure is not listed above, it is considered to be a non-standard procedure, and is therefore probably banned.

Here are some specific examples of banned procedures:

- [Noise reduction](donts/noise%20reduction.md) (*any method except binning*)
- [Sharpening](donts/sharpening.md)
- [Median filtering](donts/median%20filtering.md)
- [Normalization](donts/normalization.md) (*continuum rectification*)
- [Mosaicing](donts/mosaicing.md)
- [Heliocentric correction](donts/radial%20velocity%20correction.md)
- [Telluric subtraction](donts/telluric%20subtraction.md)

For more insight as to why these procedures are banned, see [Three Rules for Quality Spectra](three%20rules%20for%20quality%20spectra.md).

## Contact

If you have any questions about these guidelines, including whether a procedure not listed above is allowed, please email aavso@aavso.org.
