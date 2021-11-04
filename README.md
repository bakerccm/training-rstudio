# training-rstudio

This repo holds binder files to create Rstudio binders that can be used for online interactive workshops.

## Binders

- This binder (on `basic-rstudio`) only has R installed:

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/bakerccm/training-rstudio/basic-rstudio?urlpath=rstudio)

- This binder (on `rstudio-snakemake`) has R, snakemake-minimal, and some variant calling software installed:

[![Binder](https://binder.pangeo.io/v2/gh/bakerccm/training-rstudio/rstudio-snakemake?urlpath=rstudio)

- This binder (on `conda-workshop`) has Rstudio, and includes example code files for conda workshop:

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/bakerccm/training-rstudio/conda-workshop?urlpath=rstudio)

## Adding new binders from this repo

If you'd like to build a new Rstudio binder from this repo:

1) create a new branch
2) edit `environment.yml` file in the [./binder](./binder) directory
3) build a [new pangeo binder](https://binder.pangeo.io/) - remember to enter the correct Github branch!

![](./rstudio-binder-setup.png)

4) add the binder badge + brief description to this readme doc (including the repo branch)

**Important reminders:**

- `r-base` or some r package (e.g., `r-ggplot2`) needs to be in the `environment.yml` file so that R is installed during binder build
- in the pangeo binder form:
  - specify Github branch to point binder to
  - change "Path to a notebook file (optional)" dropdown to "URL" from "File". Type `rstudio` so the binder opens Rstudio.
- do not merge branches to `main` or delete branches that existing binders are pointing to, otherwise those binders will not work anymore!

---

Maintained by [Chris Baker](https://github.com/bakerccm)

Originally derived from [NIH-CFDE training materials](https://github.com/nih-cfde/training-rstudio-binder)
