# *Don't:* Noise reduction

"Noise reduction" refers to the process of using software tools on photographs or 1D spectra in order to make them look smoother and less noisy. These software algorithms are not designed for scientific spectroscopy, and with only two exceptions, **using them will invalidate the data**.

###### IMAGE: Example showing noise reduction being applied to an image in Photoshop.

[Median filtering](median%20filtering.md) is a type of noise reduction.

## Why not?

- [Rule #2a: Respect the data / Avoid small-scale alterations](../three%20rules%20for%20quality%20spectra.md)
  - Almost all noise reduction tools are designed with aesthetics in mind, not science. As a result, they operate on the scale of one to several pixels, distorting the brightnesses and shapes of spectral features.
- [Rule #3: Leave analysis to the end user](../three%20rules%20for%20quality%20spectra.md)
  - Even if a certain noise reduction algorithm is sometimes useful for scientific analysis, the decision about whether or not to apply it should be left up to the end user.

## What should I do instead?

For the purposes of AVSpec, there are only two ways to reduce noise without invalidating the data:

- [Stacking](../dos/stacking.md)
- [Binning](../allowed/binning.md)

Both stacking and binning preserve the integrity of the spectrum.

### Rule of thumb

If it is applied via software, is not stacking or binning, and makes the spectrum look less noisy, it's considered "noise reduction" by AVSpec, and is banned.
