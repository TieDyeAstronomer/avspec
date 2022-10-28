# Contaminant removal

If your spectrum is contaminated by a small artifact, like a cosmic ray, hot pixel, or background star, you can remove it by deleting just the few pixels which were affected. This is known as contaminant removal.

## Why remove contaminants?

Sometimes, you may record a great spectrum which has a small blip of contamination. Because you have access to the raw image, you can tell that the feature is definitely not part of the star's spectrum, but the end user might not know that. Removing the contamination will prevent confusion and misinterpretation.

###### IMAGE: Side-by-side example of a spectrum impacted by a hot pixel, illustrating the above paragraph. In addition to the before/after of the profile, the original image data is shown, to make it clear that the feature is a hot pixel.

## Which spectra should have contaminants removed?

All target spectra which contain small contaminants should have those contaminants removed.

For reference spectra, as long as the contamination does not impact the normal use of the spectrum (for example, extracting a continuum), contaminants do not need to be specifically removed.

## How much contamination is too much?

If the contamination covers only a few pixels, like a cosmic ray, hot pixel, or background star, it should be snipped before uploading to AVSpec. These kinds of small contamination should be relatively uncommon, and are usually unavoidable.

###### IMAGE: Side-by-side example of a spectrum impacted by a background star, before and after contaminant removal.

On the other hand, if a large region of the spectrum is contaminated, you should instead try to address the root cause of the issue. Is there a light leak? Do you need to apply darks? What about background subtraction? If you are unable to fix the root cause, but are absolutely certain that the rest of the spectrum is uncontaminated, you may salvage the uncontaminated part of the data by cropping. This should not be a regular occurance.

## Tutorial

### The bottom line:

Your goal is to remove all of the pixels which are affected by the contamination, while removing as few uncontaminated pixels as possible.

### BASS

### RSpec
