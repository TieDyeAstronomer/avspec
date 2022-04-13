# Respect the data

Do your due diligence, and process each spectrum fully, but then **leave it alone**. Resist the urge to tweak endlessly and try tricks such as a sharpening or noise reduction to improve your result. If your spectrum is too noisy, the best solution is more data!

Never apply any sort of AI enhancement or photographic manipulation to a spectrum which will be used scientifically. Remember: **you can't create information that isn't there.**

# Avoid small-scale alterations

In general, the steps you take while processing the spectrum should act on the spectrum as a whole. The amount of correction applied may sometimes vary across the field of view (as in [IR correction](../corrections%20for%20scientifically%20valid%20spectra/instrument%20response%20correction.md)), but it should do so smoothly and gradually. Any sudden discontinuities in your calibrations are a warning sign for underlying issues with the data.

# Leave analysis to the user

AVSpec collects data with specific, well-described processing steps applied. We do not accept spectra with any extra analysis steps applied ([normalization](normalization.md), [heliocentric correction](radial%20velocity%20correction.md), [telluric removal](telluric%20subtraction.md), etc.), for multiple reasons:

- These steps are often uneccesary for research.
- With multiple methods available, and a lack of widespread adoption within the amateur community, consistency is difficult to enforce.
- The potential for error is high. Performing any of these steps incorrectly can lead to spectra which are invalid in subtle and hard to detect ways.

Leaving these optional steps up to the researchers using the data gives them complete control during their analysis, enhancing both accuracy and accountability.[^1]

[^1]: Of course, you can be a user of the data too--there's nothing to stop you from applying these advanced analyses to your own copies of your spectra, or to other spectra downloaded from the database! We merely ask that you do not include spectra altered in this way in your submissions.
