# Background subtraction

Background subtraction removes light pollution, airglow, and scattered light[^1] from your spectrum. It's a required step before instrument response correction.

## Why do background subtraction?

If you don't subtract the background sky from your spectra, all of the pixels will appear brighter than they should. The amount of background contamination varies across the field of view (with a slitless system, this is due to vignetting; with a slit spectrograph, it's due to the spectrum of the sky). This variation can distort the features of your spectrum, and even introduce false features.

Even if the background is completely even across the field of view, background subtraction is **required for both the target spectrum and the reference spectrum** before you can apply instrument response correction. If you don't apply background subtraction before instrument response correction, your spectra will come out distorted, sometimes subtly...

...and sometimes not!

## Which spectra need background subtraction?

- All target spectra
- All reference star spectra used for the generation of IR curves

Spectra which are used only for wavelength calibration, and nothing else, don't need to be background subtracted.

## Tutorials

No matter which method you use, **remember:** Your goal is to measure the light coming from the background sky, and subtract that light from the spectrum, without accidentally introducing false features.

### Method #1: BASS 

### Method #2: RSpec (automatic, noisy)

### Method #3: Rspec (manual, clean)


## Footnotes

[^1]: Background subtraction usually does not include dark current, which you should remove separately using [darks](darks.md) before you start this step. That said, if your dark current is low enough, and very smooth in its distribution across the frame (as in [drift scanning](../steps%20to%20capture%20a%20slitless%20spectrum/extra%20-%20drift%20scanning.md)), you can skip applying darks; background subtraction will remove the dark current as well.