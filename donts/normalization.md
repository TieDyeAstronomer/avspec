# *Don't:* Normalization

The term "normalization" can have multiple meanings.[^1] When we refer to normalization, here's what we mean:

> ***Normalization*:** the process of dividing a spectrum by its own continuum, so that the shape becomes flat and centered at y=1.

This process is also known as "continuum rectification".

## Why not?

1. Many studies require unnormalized spectra.
2. Normalization is a type of analysis, ***not*** a processing step. It breaks [Rule #3: Leave analysis to the user](in%20general.md#Leave-analysis-to-the-user).
3. Normalization changes the shape of the spectrum. Unlike [IR correction](../dos/instrument%20response%20correction.md), this process is subjective, and no two observers will normalize a spectrum in the same way.
4. Without the original continuum curve, normalization is irreversible; and without seeing the original spectrum, there is no way to judge how 'strong' the normalization was. If small features were obliterated during the normalization, the end user will have no way to know.

###### IMAGE: Side-by-side comparison showing two versions of a spectrum of an M dwarf, one normalized and one unnormalized. Labels indicate the wide MgH and CaOH bands which most amateurs are not even aware, pointing out how they are obliterated by normalization.

[^1]: Another definition of normalization, used sometimes in the research community, can be summed up as: *"changing the scale of the y-axis of the spectrum, **without** changing the shape."* Our term for that procedure is '[y-axis rescaling](../allowed/y-axis%20rescaling.md)'.
