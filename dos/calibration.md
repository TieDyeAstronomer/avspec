# Calibration[^1]

By comparing your target spectrum to a source with known wavelengths, you can label each pixel in your spectrum with a wavelength value. This process is known as calibration.

## Why do calibration?

Calibration aligns your spectra to a universal wavelength scale. Once your spectrum is calibrated, you can identify features, measure velocities and equivalent widths, and easily compare to other spectra.

## Which spectra need to be calibrated?

All spectra must be calibrated to be useful.

## Can you reuse a calibration?

You **must** create a new calibration if your equipment changes, even only slightly. Otherwise, the answer is...

***[Slitless:](../equipment%20tips/slit%20vs%20slitless.md)*** Yes! However, because the spectrum can move around in the field of view, you must re-align the calibration to each individual spectrum using a known reference point.[^2]

***[Slit:](../equipment%20tips/slit%20vs%20slitless.md)*** Yes! As long as you do not move the grating or camera, and your spectrograph does not flex, you can reuse your calibration without modifying or realigning it.[^3]

## Tutorial

### The bottom line:

Your goal is to accurately convert horizontal pixel numbers to wavelength in Angstroms. You can do this by labeling features at known wavelengths inside your target spectrum, or by labeling a known static reference spectrum, and transferring that calibration to your target spectrum.

- Avoid [overfitting](../donts/overfitting.md), which can cause spectra to match up perfectly to the lines used in the calibration, but become wildly incorrect away from those lines.

### BASS

### RSpec

[^1]: In the context of amateur spectroscopy, "calibration" refers specifically to ***wavelength calibration***, the process of converting the x-axis of a spectrum from pixel number to wavelength. (It can also be used as a noun referring to an already-converted x-axis.) Other processing steps may be referred to with similar terms (*ex.*: [darks](darks.md) and [flats](flats.md) are also known as *'calibration frames'*), but the specific term "calibration" almost always refers to the topic described on this page.

[^2]: The zero-order star image can be a useful reference point for realigning an existing calibration, as can the [telluric](../reference%20spectra/tellurics.md) O2 A bandhead.

[^3]: Reusing a calibration will not work if your spectrograph flexes or settles with altitude, so many people opt to reshoot their calibration frames frequently, particularly when working at high resolutions where shifts of a fraction of an angstrom are visible.