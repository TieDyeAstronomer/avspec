# Background subtraction

Background subtraction removes light pollution, airglow, and scattered light[^1] from your spectrum. It's a required step before [instrument response correction](instrument%20response%20correction.md).

## Why do background subtraction?

If you don't subtract the background sky light from your spectra, all of the pixels will appear brighter than they should. If every pixel were brightened by the same amount, this might not be so bad, but unfortunately, the amount of background contamination almost always varies across the field of view.[^2] Left uncorrected, these variations can distort your spectrum, and even introduce false features.

Even if the background is completely even across the field of view, background subtraction is required for both the target spectrum ***and the reference spectrum*** before you can apply instrument response correction. If you don't apply background subtraction before instrument response correction, your spectra will come out distorted, sometimes subtly...

###### IMAGE: a subtle example of continuum aberrations due to lack of background subtraction

...and sometimes not!

###### IMAGE: a less subtle example with severe "bowl shaped" continuum

## Which spectra need background subtraction?

- All target spectra
- All reference star spectra used for the generation of IR curves

Spectra which are used only for wavelength calibration, and nothing else, don't need to be background subtracted.

## Tutorial

### The bottom line:

Your goal is to measure the light coming from the background sky, then subtract that light from the spectrum, without accidentally introducing false features.

- Avoid [overfitting](../donts/overfitting.md) any features in the background.
- Avoid including light from the target spectrum in the background sample.
- Avoid including contaminating background stars in the background sample. (*slitless only*)

### BASS

### RSpec (automatic, noisy)

### Rspec (manual, clean)

[^1]: Background subtraction usually does not include dark current, which you should remove separately using [darks](darks.md) before you start this step. That said, if your dark current is low enough, and very smooth in its distribution across the frame (as in [drift scanning](../steps%20to%20capture%20a%20slitless%20spectrum/extra%20-%20drift%20scanning.md)), you can skip applying darks; background subtraction will remove the dark current to a satisfactory degree.

[^2]: With a slitless system, variations in background brightness are usually caused by vignetting (and occasionally contaminating background stars). With a slit spectrograph, variations are features in the spectrum of the night sky.
