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
- 'Snip' known contaminants, if any[^3]

(In addition to all of the basic steps required to produce a 1D spectrum profile at all)

## Recommended

- Instrument response correction
- Darks[^4]
- Stacking
- Dithering (*slitless only*)

## Allowed

- Binning
- Rescaling the y-axis[^5]
- Flux calibration

## Banned

- Mosaicing
- Median filtering[^6]
- Noise reduction (*any method but binning*)
- Sharpening
- Normalization (*continuum rectification*)
- Heliocentric correction
- Telluric subtraction

## Minimum criteria

I can suggest specific numbers for these criteria, but it's a squishy problem, and I'd rather hear some other opinions first. Thoughts?

- Maximum calibration error (1x FWHM?)
- Minimum resolution[^7] (?, *see footnote for comments*)
- Minimum SNR (?) (If enacted, should this depend on the target's type and/or magnitude?)
- *Potential alternative to the above:* Minimum number of visible features?

### Footnotes

[^1]: Background subtraction is often, but **not always** applied during initial profiling of a spectrum. It's an easy way to cut down on otherwise confusing contamination of the spectrum, it's absolutely required before IR correction can be applied, and is generally a "best practice" which should not require much extra effort at all for observers to implement.

[^2]: It is not possible to apply flats to slitless spectra with current technologies and techniques avaialble to amateurs, so it's very important that we **do not** require flats for slitless spectra. However, flats are the only way to reliably remove thin-film interference effects (which grow especially prominent at high resolution). In general, I've tried to remain equipment-agnostic with these guidelines, but given the high impact of TFI on a spectrum, I'm suggesting that we **require flats for slit spectrographs only.** The alternative would be strongly recommending flats for slit spectrographs only, in which case we would probably get some slit spectra which show severe "sine wave" distortions due to TFI ([click here for examples](http://www.astrosurf.com/buil/fringes/index.html)), but perhaps we are ok with that as long as the absence of flatting is well-recorded in the metadata?

[^3]: This would be specified as applying to 'false features' with limited spatial impact, such as cosmic rays and contaminating background stars. These sorts of contaminants can strike unpredictably, but they leave most of the spectrum untouched, so quality data can easily be salvaged by deleting only the pixels which were affected by the contamination. ([Click here](https://i.imgur.com/3oddhdx.png) for an example of what that would look like.)

[^4]: I've classified darks as "recommended, but optional" because while they are useful for improving data quality, their absence is of relatively little consequence. If darks are not applied, background subtraction takes care of broad features such as amp glow, so hot pixels become the main concern; but those are easily identifiable, and not unusual to find in professional spectra. Particularly in the case of slitless spectroscopy with a large number of dithered frames (i.e. drift scanning), the difference between spectra with and without darks is virtually unobservable.

[^5]: This simple rescaling of the y-axis is sometimes referred to as "normalization" by professionals (while "normalization" in the sense that most amateurs use is referred to instead as "continuum rectification"). Because of this potential confusion in terminology, it feels important to have guidelines for both meanings of the word (in addition to clearly stating the definition we use).

[^6]: Median filtering is the practice of averaging a pixel with its neighbors, **without** reducing the total pixel count (this is what differentiates it from binning). Median filtering results in spectra which "look" high resolution and high S/N, but which have blurred features. This could result in misinterpretation by the user of the data, who may think that a line is broadened by e.g. rotation, when it's actually an artifact of median filtering.

[^7]: Right now, at least two of our top observers are using Star Analyzers inside filter wheels to shoot spectra of faint targets concurrently with their photometry. It's important to keep in mind that if we set a global resolution limit any higher than "filter wheel SA resolution"—say, R=150—we'll effectively be banning those observers, as well as that general mode of observation, which is the only way that amateurs can observe many faint targets. As a result, I would recommend either setting a very low resolution limit, or simply leaving it up to the end user to filter for the resolution they want. (Alternatively, we could have different resolution limits at different limiting magnitudes.)
