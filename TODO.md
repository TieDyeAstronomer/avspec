# Terminology

## "Normalization" vs. "Continuum rectification"?

Which term should we use when discussing the procedure of dividing a spectrum by its own continuum in order to flatten it?

### "Normalization"

- Less intimidating
- Easier to remember for most amateurs
- Is the term in broad use in the amateur community

### "Continuum rectification"

- Is used by at least a few professional astronomers (Q: how widespread?)
- Distinguishes from another procedure which is also sometimes referred to as "normalization" (the procedure of rescaling the entire y-axis without changing the shape of the spectrum)

# Goal

We need to define highly specific guidelines for AVSpec. These guidelines would apply to the capture and processing of all spectra submitted to the database.

The guidelines should describe:

1. Specific steps which are **required** for every spectrum.
2. Specific steps which must **not** be performed on any spectrum.
3. Optional steps which are **recommended**, but not required. (*For accountability, the presence of these optional processing steps will need to be tracked using metadata either in FITS header, or the user submission form.*)
4. Optional steps which are not necessarily reccommended, but are allowed (e.g. binning).
5. Minimum qualitative criteria for the acceptance of a spectrum.

# Suggested guidelines

The guidelines below are suggested for discussion. For a few of them, I've provided my reasoning in the form of footnotes. I would love to recieve questions, suggestions, disagreements, advice... let me know what you think!

## Required

- Wavelength calibration
- Background subtraction[^1]
- Flats (*slit only*)[^2]

(In addition to all of the basic steps required to produce a 1D spectrum profile at all)

## Recommended

- Instrument response correction
- Darks[^3]
- Stacking
- Dithering (*slitless only*)

## Allowed

- Binning
- Rescaling the y-axis[^4]
- Flux calibration

## Banned

- Median filtering[^5]
- Noise reduction (*any method but binning*)
- Sharpening
- Normalization (*continuum rectification*)
- Heliocentric correction
- Telluric subtraction

## Minimum criteria

- Maximum calibration error - 1x FWHM?
- Minimum resolution(?)
- Minimum SNR(?) (If enacted, should this depend on the target's type and/or magnitude?)

[^1]: Background subtraction is often, but **not always** applied during initial profiling of a spectrum. It's an easy way to cut down on otherwise confusing contamination of the spectrum, it's absolutely required before IR correction can be applied, and is generally a "best practice" which should not require much extra effort at all for observers to implement.

[^2]: It is not possible to apply flats to slitless spectra with current technologies and techniques avaialble to amateurs, so it's very important that we **do not** require flats for slitless spectra. However, flats are the only way to reliably remove thin-film interference effects (which grow especially prominent at high resolution). In general, I've tried to remain equipment-agnostic with these guidelines, but given the high impact of TFI on a spectrum, I'm suggesting that we **require flats for slit spectrographs only.** The alternative would be strongly recommending flats for slit spectrographs only, in which case we would probably get some slit spectra which show severe "sine wave" distortions due to TFI ([click here for examples](http://www.astrosurf.com/buil/fringes/index.html)), but perhaps we are ok with that as long as the absence of flatting is well-recorded in the metadata?

[^3]: I've classified darks as "recommended, but optional" because while they are useful for improving data quality, their absence is of relatively little consequence. If darks are not applied, background subtraction takes care of broad features such as amp glow, so hot pixels become the main concern; but those are easily identifiable, and not unusual to find in professional spectra. Particularly in the case of slitless spectroscopy with a large number of dithered frames (i.e. drift scanning), the difference between spectra with and without darks is virtually unobservable.

[^4]: This simple rescaling of the y-axis is sometimes referred to as "normalization" by professionals (while "normalization" in the sense that most amateurs use is referred to instead as "continuum rectification"). Because of this potential confusion in terminology, it feels important to have guidelines for both meanings of the word (in addition to clearly stating the definition we use).

[^5]: Median filtering is the practice of averaging a pixel with its neighbors, **without** reducing the total pixel count (this is what differentiates it from binning). Median filtering results in spectra which "look" high resolution and high S/N, but which have blurred features. This could result in misinterpretation by the user of the data, who may think that a line is broadened by e.g. rotation, when it's actually an artifact of median filtering.
