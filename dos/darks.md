# Dark frames

If you block all light from entering a camera, then take a photo, you get a dark frame: a photograph with nothing in it except the camera's own noise. By subtracting this dark frame from your spectrum image, you can remove the effects of this unwanted light.

## Why use darks?

Darks remove thermal noise, amp glow, and hot pixels from your images. If you don't apply darks, these sources of noise can cause false features in your spectrum, and/or skew the continuum.

## Which spectra need to be darked?

Not all spectra *need* to be darked, but it will never hurt your spectrum to use darks.

If you are stacking more than 100 images which are [dithered](dithering.md), (as in the case of drift scanning), darks will have little impact on the result. However, it will not hurt to use darks anyway.

AVSpec reccommends that you use darks, but they are **not** required.

## Can you reuse darks?

Yes. The important thing is that your darks are taken at the same temperature as your spectrum. Some people take new darks every year. ***[[[[Look into how often advanced amateur spectroscopists take darks]]]]***

Here are some situations when you should take new darks:
- If you get a new camera.
- If you change your binning factor.
- If you don't have existing darks taken at the same temperature as your spectrum.

## Tutorial

You can create a dark frame by shooting a long exposure with **absolutely no light** entering the camera.
