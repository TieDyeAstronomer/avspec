# *Don't:* Sharpening

Sharpening is a photographic technique which is sometimes applied to spectra in an attempt to make spectral features clearer and easier to see. While certain forms of sharpening may sometimes be used during scientific analysis, sharpening is **never** allowed for spectra submitted to AVSpec.

## Why not?

- [Rule #2a: Respect the data / Avoid small-scale operations](../three%20rules%20for%20quality%20spectra.md)
  - Sharpening is a destructive operation which alters the individual pixel values, distorting spectral features.

## What should I do instead?

Instead of using software, you can increase your spectral resolution by modifying your equipment. Here are some options to consider:

### If you're using a slitless grating

- Use a wedge prism to reduce blur from [spectral coma](../identifying%20aberrations/spectral%20coma.md).
- Increase the spacing between your grating and camera to magnify the spectrum more.
- For resolutions of R>600, consider upgrading to a slit spectrograph.

### If you're using a slit spectrograph

- Use a smaller slit if your spectrum is [oversampled](../identifying%20aberrations/oversampling.md).
- Use a camera lens with a longer focal length to magnify the spectrum more.
- Consider upgrading to a higher resolution spectrograph.

You can also try reducing noise by increasing your exposure time, [stacking](../dos/stacking.md) more frames, and/or dithering. Noisy spectra naturally look lower resolution, so reducing noise will allow you to realize the full potential of your current resolution.
