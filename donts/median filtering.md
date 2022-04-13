# *Don't:* Median filtering

Median filtering is a simple form of [noise reduction](noise%20reduction.md), applied by setting every pixel's brightness to the median of its neighbors. The result is a spectrum which has the same number of pixels in it, but appears blurrier.

###### Image: before and after example of median filtering, on both images and profiles

As a simple arithmatic operation applied equally across the image, median filtering is not as bad as other methods of noise reduction, and can be a useful tool during analysis.

However, **median filtering should never be applied to spectra which are submitted to AVSpec.** Median filtering changes the shape of the data in a way which is difficult to detect, and violates [Rule #3: Leave analysis to the user](in%20general.md#Leave-analysis-to-the-user).