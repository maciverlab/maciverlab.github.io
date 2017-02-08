---
title: A massive increase in visual range preceded the origin of terrestrial vertebrates
data
paper: bigeye
categories: bigeye
---

## Hydrolight

HydroLight is a commerical product of [Sequoia Scientific, Inc.](www.hydrolight.info). The HydroLight software solves the scalar radiative transfer equation (SRTE) using user-supplied inputs that describe the water absorption and scattering properties, surface wave state, incident sky lighting, and bottom reflectance.  The software comes with many sub-models and databases for absorption and scattering by biological and mineral particles and dissolved substances, sky irradiance, and bottom reflectance by various materials.  To perform a run, the user works through the user interface to specify the desired environmental conditions.  This can be done in many ways depending, for example, on whether the user chooses to accept various defaults or wishes to input the user's own data sets or analytical models for quantities such as the spectral absorption and scattering properties of the water constituents (pure water, phytoplankton, dissolved substances, mineral particles, etc.).  In any case, after making the selections that define the radiative transfer problem to be solved, the user interface writes the information to an ascii file generically named Iroot.txt, where in a particular run, "root" is replaced by a user-defined name that is used to identify the run.  The Iroot.txt file then becomes the input to the HydroLight core mathematical code that solves the SRTE.

The files included here contain the Iroot.txt input files, and multiwavelength-format Excel files (Mroot.txt), for the various simulations used in this study.  The runs for moonlight and starlight also contain input datafiles for moonlight and starlight sky spectral irradiances, which are not part of the standard HydroLight distribution.  These files make it possible to reproduce the runs used in this study, once HydroLight has been licensed and installed.  The files are organized by the water types of the runs: "baseline" for the baseline run with typical water optical properties, “Clear" for the very clear water case, “ScatDom” for the scattering dominated water type, and so on.


## Images for contrast analysis

From Google images various images of millipedes, centipedes and fresh water fish were found to calculate naturalistic contrast values. These images can be found in the folder [imagecontrast](https://github.com/maciverlab/bigeye/tree/master/figs/data/vision/imagecontrast).