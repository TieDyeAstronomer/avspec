# Instrument response correction (IR correction)

Everything that you can see, from the lenses and mirrors in your telescope to the air that we breathe, has a color. That means that when light shines through, some wavelengths are absorbed more than others, making even the best spectra naturally come out unevenly bright. IR correction removes these irregularities, shaping the continuum of your spectrum to match a standard star.

## Why do IR correction?

IR correction removes the 

## Which spectra need IR correction?

IR correction is encouraged, but is ***not*** required for spectra submitted to AVSpec.

Even for purely personal use, there is no need to IR correct spectra which are used only for calibration purposes.

## How often should you create IR curves?

Because the IR curve is a combination of all the things here on Earth that the light passed through—including the atmosphere, your telescope, your spectrograph, and your camera—it should be updated every time one of those things changes.

You probably don't switch telescopes very often, but the atmosphere is constantly changing, so in an perfect scenario, you should create a new IR curve for every target. But of course, creating a new IR curve takes a lot of time and effort. In practice, if all of your targets are placed far above the horizon where atmospheric effects are low, and the conditions are not changing, you can safely use the same IR curve all night.

## Tutorial

### The bottom line:

To create an IR curve, you will observe a standard star, then compute the difference between what you observed and what the spectrum should theoretically look like.

To apply the IR curve, you will divide your target spectrum by the IR curve.

For help choosing a standard star, see [Selecting a standard star](../selecting%20a%20standard%20star.md).

- Avoid [overfitting](../donts/overfitting.md), which can result in smoothing out real features in the spectrum.

### Bass

### RSpec
