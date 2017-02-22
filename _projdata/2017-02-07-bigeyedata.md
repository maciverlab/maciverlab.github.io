---
title: Massive increase in visual range preceded the origin of terrestrial vertebrates data
paper: bigeye
categories: bigeye
---

To do:
rename file names

## Morphological and phylogenetic data for eye-orbit correlation

To better understand the correlation betwen the bony eye socket and soft 
tissue dimensions of the eye we collected measurements in teleost fish. We provide these 
morphological measurements in CSV files, named "mean_ol_ed_pd_0502.csv" **(needs hyperink)** (for eye diameter) 
and "mean_ol_ed_pd_0709.csv" **(needs hyperlink)** (for pupil diameter).

In oder to perform this statistical description with incorporation of phylogenetic 
covariance, we also provide a tree-file for a species-level, time-calibrated fish 
phylogeny from [Rabosky et al. 2013, Nature Communications](https://github.com/maciverlab/bigeye/blob/master/literature/Rabo13a_rates_speciation.pdf) [“fish.tre”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/fish.tre).

## Phylogenetic data for tetrapod analysis

The basic topology of our tree is provided in the tree-file [“bigeye0527.tre”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/bigeye0527.csv). For time-calibration,
you will need the stratigraphic ranges of the taxa, which can be found in the CSV-file [“sampled.alt.csv”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/sampled.alt.csv).
A full set of 1000 trees is available in [“alt.equal.trees.tre”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/alt.equal.trees.tre).

## Morphological data for tetrapod analysis

Measurements of skull length and eye socket length in tetrapods are in the CSV-file [“bigeye0527.csv”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/bigeye0527.csv),
formatted for easier handling in R. Residuals of eye sockets on skull length, obtained from PGLS with 
Brownian motion correlation structure are provided in [“BMres.csv”](https://github.com/maciverlab/bigeye/blob/master/figs/data/paleo/BMres.csv). 

## Skull Images

All the skull images with superimposed measurement indicator (as provided in the supplement) used in this study can be found in the folder [*skull_measurements*](https://github.com/maciverlab/bigeye/tree/master/figs/data/paleo/skull_measurements). Moreover, raw skull images are also available in folder [*skulls_raw*](https://github.com/maciverlab/bigeye/tree/master/figs/data/paleo/skulls_raw).

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