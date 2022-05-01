# Terminology which needs to be officially defined

I need input from the AVSpec working group to find out if there are strong opinions either way on which terms we should use throughout these documents.

## "Researcher" vs. "End user"?

Which term should we use to refer to a user of AVSpec's data?

### Researcher

>*"If features are missing, a researcher will have no way to know."*

- Reinforces the concept that if you submit spectra, they will be used for real science.

### End user

>*"If features are missing, the end user will have no way to know."*

- Reinforces the fact that anyone (including you!), can analyze data from AVSpec.

## "Normalization" vs. "Continuum rectification"?

Which term should we use when discussing the procedure of dividing a spectrum by its own continuum in order to flatten it?

### Normalization

>*"Normalization changes the shape of the spectrum."*

- Less intimidating
- Easier to remember for most amateurs
- Is the term in broad use in the amateur community

### Continuum rectification

>*"Continuum rectification changes the shape of the spectrum."*

- Is used by at least a few professional astronomers (does anyone know how widespread?)
- Distinguishes from another procedure which is also sometimes referred to as "normalization" (the procedure of rescaling the entire y-axis without changing the shape of the spectrum)

## Writing as an authority: "AAVSO" vs "AVSpec"?

When referring to decisions which have been made about submission criteria, should we refer to these decisions as having been made by "the AAVSO" or "AVSpec"? Put another way: who should be the 'authority' referred to consistently throughout the documentation?

### AAVSO

>*"The AAVSO neither recommends nor forbids y-axis rescaling."*

- &#10003; Makes AVSpec sound more clearly like a piece of tech run by the AAVSO.
- &#10007; Might cause the docs to sound more ambiguous.
  - "AVSpec" will still be used to refer to the database/website itself, so someone more unfamiliar with the AAVSO might wonder if the example sentence above applies only to AVSpec, or to many projects run by the AAVSO, or to other projects but not AVSpec...

### AVSpec

>*"AVSpec neither recommends nor forbids y-axis rescaling."*

- &#10003; Would unify the voice of the documentation, making it clear that everything referred to definitely applies to AVSpec.
- &#10007; Makes AVSpec sounds more like an independent project, possibly with its own staff.
