# Calibration

By comparing your spectrum to a source with known wavelengths, you can label each pixel in your spectrum with a wavelength. This process is known as calibration[^1].

## Why do calibration?

Calibration aligns your spectra to a universal wavelength scale. Once your spectrum is calibrated, you can identify features, measure velocities and equivalent widths, and easily compare to other spectra.

## Which spectra need to be calibrated?

All spectra must be calibrated to be useful.

## FAQ

### 1. Can I reuse a calibration?

You **must** create a new calibration if your equipment changes, even only slightly. Otherwise, the answer is...

***[Slitless:](../equipment%20tips/slit%20vs%20slitless.md)*** Yes! In fact, reusing your calibrations is encouraged.[^2] However, because the spectrum can move around in the field of view, you must re-align the calibration to each individual spectrum using a known reference point.[^3]

***[Slit:](../equipment%20tips/slit%20vs%20slitless.md)*** Yes! As long as you do not move the grating or camera, and your spectrograph does not flex, you can reuse your calibration without modifying or realigning it.[^4]

### 2. Should I use a linear or nonlinear calibration?

You should use a **linear** calibration if...

- You are using a slitless grating.
- You have carefully measured your slit spectrograph's wavelength solution, and found it to be linear to a high degree of accuracy.

You should use a **nonlinear** calibration if...

- You are using a slitless grating **with** a corrective prism.
- You are using a slit spectrograph.

### 3. What do I need to create a calibration?

#### Slitless gratings & low resolution slit spectrographs:

You can use almost any bright star to create a calibration. [Standard stars](../selecting%20a%20standard%20star.md) such as Vega are a great choice, because their continuums are smooth, making it easy to identify calibration features. (As a bonus, you can also use the standard star spectrum to create an [IR curve](instrument%20response%20correction.md).)

#### High resolution slit spectrographs:

A calibration lamp is the best way to create a calibration for a high resolution slit spectrograph. If your spectrum was taken in the red or infrared, you can also create a high quality calibration using [telluric](../reference%20spectra/tellurics.md) lines.

You should not use a stellar spectrum to create your calibration, unless the star has a known radial velocity which is far too small for your spectrograph to detect.

## Tutorial

### The bottom line:

Your goal is to accurately convert horizontal pixel numbers to wavelength in Angstroms. You can do this by labeling features at known wavelengths inside your target spectrum, or by labeling a known static reference spectrum, and transferring that calibration to your target spectrum.

- Avoid [overfitting](../donts/overfitting.md), which can cause spectra to match up perfectly to the lines used in the calibration, but become wildly incorrect away from those lines.

### BASS

### RSpec

[^1]: In the context of amateur spectroscopy, "calibration" refers specifically to ***wavelength calibration***, the process of converting the x-axis of a spectrum from pixel number to wavelength. (It can also be used as a noun referring to an already-converted x-axis.) Other processing steps may be referred to with similar terms (*ex.*: [darks](darks.md) and [flats](flats.md) are also known as *'calibration frames'*), but the specific term "calibration" almost always refers to the topic described on this page.

[^2]: It is not always possible to calibrate the spectrum of a star accurately by looking at its spectral features. It may be redshifted or blueshifted, have strange line profiles, or have few visible features. For this reason, we recommend that instead of creating a new calibration for each target star, observers should focus on creating a single, high quality calibration, then reuse that calibration whenever possible. (This does not apply to observers who use calibration lamps.)

[^3]: The zero-order star image can be a useful reference point for realigning an existing calibration, as can the [telluric](../reference%20spectra/tellurics.md) O2 A bandhead.

[^4]: Reusing a calibration will not work if your spectrograph flexes or settles with altitude, so many people opt to reshoot their calibration frames frequently, particularly when working at high resolutions where shifts of a fraction of an angstrom are visible.
