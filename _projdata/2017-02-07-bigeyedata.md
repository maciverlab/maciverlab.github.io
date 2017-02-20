---
title: Massive increase in visual range preceded the origin of terrestrial vertebrates data
paper: bigeye
categories: bigeye
---

To do:
Add the paleo data


## HydroLight

HydroLight is a commercial product of [Sequoia Scientific, Inc.](http://www.sequoiasci.com). The HydroLight software solves the scalar radiative transfer equation (SRTE) using user-supplied inputs that describe the water absorption and scattering properties, surface wave state, incident sky lighting, and bottom reflectance.  The software comes with many sub-models and databases for absorption and scattering by biological and mineral particles and dissolved substances, sky irradiance, and bottom reflectance by various materials.  To perform a run, the user works through the user interface to specify the desired environmental conditions.  This can be done in many ways depending, for example, on whether the user chooses to accept various defaults or wishes to input the user's own data sets or analytical models for quantities such as the spectral absorption and scattering properties of the water constituents (pure water, phytoplankton, dissolved substances, mineral particles, etc.).  In any case, after making the selections that define the radiative transfer problem to be solved, the user interface writes the information to an ascii file generically named Iroot.txt, where in a particular run, "root" is replaced by a user-defined name that is used to identify the run.  The Iroot.txt file then becomes the input to the HydroLight core mathematical code that solves the SRTE.

The files included here contain the Iroot.txt input files, and multiwavelength-format Excel files (Mroot.txt), for the various simulations used in this study.  The runs for moonlight and starlight also contain input data files for moonlight and starlight sky spectral irradiances, which are not part of the standard HydroLight distribution.  These files make it possible to reproduce the runs used in this study, once HydroLight has been licensed and installed.  

The files are organized by the water types of the runs: 

* “base_sun” for the baseline run with typical water optical properties under clear sky sunlight
* “base_moon” for the baseline run with typical water optical properties under clear sky moonlight
* “base_starlight” for the baseline run with typical water optical properties under clear sky starlight

The data for sensitivity analysis on the effects of different optical water properties can be found in folders named according to run:

* “Clear" for the very clear water case, 
* “ScatDom” for the scattering dominated water type,
* “AbsDom” for absorption dominated water type,
* “HighTurbidity” for turbid water type


## Images for contrast analysis

From Google images various images of millipedes, centipedes and fresh water fish were found to calculate naturalistic contrast values. These images can be found in the folder [imagecontrast](https://github.com/maciverlab/bigeye/tree/master/figs/data/vision/imagecontrast).

## Literature

Most of the cited literature except some books and monographs can be found in the [literature folder](https://github.com/maciverlab/bigeye/tree/master/literature). The publications are titled with format: first four letters of author last name last two digits of publication year and part of the title (eg. MacIver, Malcolm A., Noura M. Sharabash, and Mark E. Nelson. "Prey-capture behavior in gymnotid electric fish: motion analysis and effects of water conductivity." *Journal of experimental biology* 204.3 (2001): 543-557.
in pdf form is: MacI01a_prey_capture_behavior_gymanotid_el_4500.pdf)</p>