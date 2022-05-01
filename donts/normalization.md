# *Don't:* Normalization

The term "normalization" can have multiple meanings.[^1] When we refer to normalization, here's what we mean:

> *Normalization*: the process of dividing a spectrum by its own continuum, so that the shape becomes flat and centered around y=1.

This process is also known as "continuum rectification".

## Why not?

1. Many studies require unnormalized spectra.
2. Normalization is a type of analysis, ***not*** a processing step. It breaks [Rule #3: Leave analysis to the user](in%20general.md#Leave-analysis-to-the-user).
3. Normalization changes the shape of the spectrum. Unlike IR correction, this process is subjective, and no two observers will normalize a spectrum in the same way.
4. Without the original continuum curve, normalization is irreversible; and without seeing the original spectrum, there is no way to judge how 'strong' the normalization was. If small features were obliterated during the normalization, the end user will have no way to know.

[^1]: Another definition of normalization, used sometimes in the research community, can be summed up as: *"changing the scale of the y-axis of the spectrum, **without** changing the shape."* Since this kind of normalization does not alter the shape of the spectrum, and the y-axis units are virtually always arbitrary anyway, spectra which are "normalized" in this simple way are perfectly acceptable for AVSpec.