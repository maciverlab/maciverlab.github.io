---
title: Massive increase in visual range preceded the origin of terrestrial vertebrates
paper: bigeye
categories: bigeye
---
<br><br>
[![DOI](https://zenodo.org/badge/76398715.svg)](https://zenodo.org/badge/latestdoi/76398715)
<br><br>
## Generating the summary of our phylogenetic comparative study

You can visualize the main results of our phylogenetic comparative analysis (similar to Fig. 2) by executing the code in folder [fig02_phylo_orbit](https://github.com/maciverlab/bigeye/tree/master/figs/fig02_phylo_orbit) in the project GitHub. The script plots the phylogeny of the species in our analysis, scaled against geologic time, and illustrates the residual eye socket size of early tetrapods by adding scaled dots to the tips. It also highlights the branches along which we found support for changes in the selective regime of eye socket evolution. These branches were identified with bayou, an R package for characterizing the dynamics of adaptive landscape. Note that we are summarizing results over a set of 1000 trees. The major differences between the trees concern the time-scaling, and the topology of three unresolved parts of the tree. These polytomies were resolved randomly and branches in these parts of the tree did not feature well-supported shifts in eye socket size evolution.To run the code, go to the directory of the script in terminal/command prompt and type…

```
$ Rscript fig02.R --cwd
```

This script will output the following figure (saved as pdf):


![Summary of our phylogenetic comparative study]({{ site.url }}/assets/fig02.png)


### Full phylogenetic comparative analysis

If you would like to run the full phylogenetic comparative analysis with the same settings that we used for the paper, you can run the code in folder ‘bayou’. Depending on your computer the script may run for a few days. Open the terminal in the bayou folder to initiate the analysis…```$ Rscript bayou_parallel_BM.R --cwd
```

The results will be saved at the end of the run in the bayou folder. You can change the settings of the analysis by modifying the original R code; please let us know if we can help with that. If you would like to run the analysis with residuals obtained from regression in an Ornstein-Uhlenbeck framework (as opposed to Brownian motion), you can run this script:```
$ Rscript bayou_parallel_OU.R --cwd```

### Diagnostic tests

We performed several diagnostic tests to ensure that convergence of the two reversible jump mcmc chains was achieved, which are shown in the Supplementary Appendix Figure S3. One such characteristic is Gelman’s R, which we calculated for logLikelihood, alpha, and sigma^2. You can reproduce an example of this by executing the code in folder [fig03Ext_abc](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03abc_gelman). Open the terminal in that folder and type this command…```$ Rscript figExt03_abc.R --cwd
```![Gelmans R]({{ site.url }}/assets/figExt_03abc.png)


The fourth panel of this plot shows a bivariate plot of the posterior probabilities of a selective regime shift along a branch from both chains. If convergence is achieved, the dots should fall roughly along a line. In the figure below, we have summarized the posterior probabilities from both chains for all branches across all trees. To make the plot more legible, we shaded the high density areas instead of plotting every single point. Open the terminal in folder [figExt03_d](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03d_PP) to run the script…

```$ Rscript figExt03_d.R --cwd
```

![Posterior probabilities]({{ site.url }}/assets/figExt_03d.png)

To further visualize bayou results we provide scripts to plot frequency distribution of posterior probabilities of rate shifts along branches and the estimated peak eye socket sizes for selected branches in folders [figExt03e_freq](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03e_freq) and [figExt03_f_peaks](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03f_peaks).

## Eye socket lengths across the taxa

Skull measurements from published drawing and images produced by experts in the field were collected. Eye socket length is defined as the maximum length of the socket, except for taxa in the digited tetrapod group featuring antorbital vacuities, for which the major axis of an ellipse fit to the orbit alone was used. We define skull length as the distance from the tip of the snout to the caudal margin of the postparietal bones, at their medial suture.


Skull images used can be found in the Supplementary Appendix.


Directory titled [fig03_socket_length](https://github.com/maciverlab/bigeye/tree/master/figs/fig03_socket_length) has the main code to plot eye socket sizes across taxa. The function named [fig03a_socketlength](https://github.com/maciverlab/bigeye/tree/master/figs/fig03a_socket_length writes a text file with calculated stat values (mean, standard deviation and sample size) ,creates two data files:

1. List of eye socket lengths for 4 groups (finned, finned-transitional, digited, and digited-aquatic)
2. List of orbit lengths for finned and digited tetrapods

and outputs and saves a pdf with the plot for absolute eye sizes in mm across the groups created by trait evolution.

In order to execute the code in Matlab, simply type:


``` Matlab
run fig03_socketlength
```

The output figure will be:

![Eye socket lengths across taxa]({{ site.url }}/assets/fig03.png)

Relative eye socket size was calculated as residuals from a phylogenetically informed regression of log10-transformed variables, averaged over the full set of 1,000 trees. Positive residuals indicate eye sockets larger than expected based on skull length, whereas negative residuals indicate eye sockets smaller than expected.As expected for a diverse group, not all tetrapods are at their respective peak, reflecting a normal evolutionary pattern where trait values are dispersed around the optimal value. The Bayesian OU findings show that there must have been a selective benefit from larger eye sockets in finned-transitional and digited tetrapods, but uncovering its basis requires modeling visual performance across likely environments.

The for each specie is saved in a csv file titled BMres.csv and is the output of the R script that can be found in folder [fig03b_data](https://github.com/maciverlab/bigeye/tree/master/figs/fig03b_data). The R script can be executed through the command line by typing:

```
$ Rscript gettingBMres.R —cwd
```

The species and corresponding residuals were then grouped according to the trait evolution. 


## Computational visual ecology


The numerical model for both aquatic and aerial vision contains two components: calculation of the optical stimulus, which can overestimate visual range (particularly in the aerial case), and calculation of the effect of contrast threshold. The framework for calculation of the optical stimulus is adapted from Nilsson et al., which calculates visual range based on the assumption that there are two separate channels that view the background and the target, where channel size is determined by the angular size of the target on the retina (given a particular photoreceptor arrangement) for optimal viewing. 

However, visibility of an object is dependent on the apparent contrast of the object, and the observer’s contrast threshold. Contrast follows the same attenuation law as light, and therefore the object’s perceived contrast in absolute value is less than its inherent contrast. The governing law in vision then becomes: if an object’s apparent contrast at a given range is smaller than the observer’s contrast threshold the object is said to invisible.


The set of functions provided in folder [fig04_visualrange](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange) calculate:

1. Visual range for a 10cm disk in aquatic and aerial environments, for photopic, scotopic and mesopic viewing conditions
2. Visual sensory volume which is estimated by a spherical sector with radius equal to visual range, azimuth equal to 305º for aquatic and 287º for aerial, and elevation equal to 60º for aquatic and 30º for aerial vision.
3. Derivatives of both visual range and visual sensory volume with respect to pupil size, which are used as a proxy for performance/gain.


Parent folder (fig04_visualrange) has three subdirectories: [aquatic_model](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/aquatic_model), [aerial_model](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/aerial_model), and [figure_sensitivity](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/figure_sensitivity). 


Figure folder has two functions that execute: 

1. Calculation of percent difference between visual range obtained from varying parameters and original parameter values
2. Generation of figure pdf that takes in the optional boolean argument *CONTRASTTHRESH*. If true, visual range that is calculated based on contrast threshold is plotted, and if false, visual range that is based on firing threshold is represented. The default value of *CONTRASTTHRESH* is set as true. 


``` Matlab
run fig04_visualrangeWsensitivity
```

The execution of the above function generates the following figure:

![Visual range and performance for aquatic and aerial conditions]({{site.url}}/assets/fig04.png)


The subdirectories *aquatic_model* and *aerial_model* contain the functions that calculate visual range based on firing and contrast threshold. Parameter values shown in Supplementary Appendix Table S1 can be modified in [Parameters.m](https://github.com/maciverlab/bigeye/blob/master/figs/data/vision/Parameters.m) found under *figs/data/vision/*.


### Example run:

If we take the aquatic vision calculations as an example, the primary folder that has the relevant code is [aquatic_model](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/aquatic_model). Under this folder the functions *Aquatic_firingThresh.m* and *Aquatic_contrastThreshold.m* calculate visual range based on the firing and contrast threshold methods explained in detail in the Supplementary Appendix.  


*Aquatic_firingThresh.m* calculates visual range for upward and horizontal viewing directions for daylight, moonlight and starlight conditions based on the optical stimulus that reaches the eye. It generates the data file *meteoAquatic.mat* that has an array of discrete pupil values used and corresponding visual range values (1st dimension is across pupil diameters, 2nd dimension is across light conditions and 3rd dimension is across viewing direction). 


*Aquatic_contrastThresh.m* checks to see if *meteoAquatic.mat* exists, and if it does, given pupil diameter, viewing direction, light condition and corresponding visual range, the algorithm iteratively calculates apparent contrast of the object and observer’s contrast and checks to see if the object is visible. If the object is invisible (apparent contrast is below the contrast threshold) visual range is decreased, and the whole process is repeated. 


*Aquatic_calcVolumegetDer.m* takes in the optional *CONTRASTTHRESH*, which if true loads *visibilityAquatic.mat* and if false loads the data *meteoAquatic.mat*, where the default value is set to be true. The function calculates and returns visual volume from a spherical sector, and derivatives of visual range and visual volume with respect to pupil diameters in mm. 

A correct sequence of runs therefore would be:


```Matlab
run Aquatic_firingThresh
run Aquatic_contrastThresh
run Aquatic_calcVolumegetDer
```

The folder titled [parameter_sensitivity](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/aquatic_model/parameter_sensitivity) within *aquatic_model* folder calculates visual range for only daylight, based on alternative values given in Supplementary Appendix Table S2. The provided functions calculate visual range and performance metrics, for which visual range is saved separately based on the model used. 


*Aquatic_Sensitivity.m* calculates visual range based on optical stimulus and contrast threshold, and creates two data files *meteoAquaticSensitivityParameters.mat* (visual range based on firing threshold) and *visibilityAquaticSensitivityParameters.mat* (visual range based on contrast threshold) . These data files have an array of pupil values and corresponding visual ranges (1st dimension is across pupil diameters, 2nd dimension across viewing direction, and 3rd dimension across perturbed parameters). It is important to note that the contrast threshold perturbation is not calculated within this function.


*Aquatic_contrastThreshSensitivity.m* calculates visual range based on the visibility (contrast threshold) model, where the observer’s contrast threshold is increased by 15%. 


*Aquatic_calcVolumegetDerSensitivity.m* behaves exactly the same as *Aquatic_calcVolumegetDer.m*. 

A sample run would look like:


```Matlab
run Aquatic_Sensitivity
run Aquatic_contrastThreshSensitivity
run Aquatic_calcVolumegetDerSensitivity
```

Similar runs with equivalent function definitions can be performed with the [aerial model](https://github.com/maciverlab/bigeye/tree/master/figs/fig04_visualrange/aerial_model).


In the [figure_sensitivity](https://github.com/maciverlab/bigeye/blob/master/figs/fig04_visualrange/figure_sensitivity/calculatePercentChange.m) folder, in addition to the main figure generating file there’s a helper function that calculates percent change due to parameter perturbations (*calculatePercentChange.m*). For each performance parameter, percent difference caused by changes to the model parameters were calculated and stored in *percChange.mat*. 


Once the figure generation file *fig04_visularange* is executed in Matlab, it will search through all the directories to see if the data files are available, and if they are, it will ask the user if they want to re-run all of the code and regenerate visual ranges. If they are not, it will run the corresponding function to the missing data file. Once the data files are available they will be loaded and the figure will be drawn. 

## Eye and eye socket size in teleost fishesTo further explore the correlation of eye soft tissue structures to the bony eye socket, we turned to teleost reef fishes. We specifically were interested in the correlation between eye socket and eye diameter, as well as eye socket and pupil diameter. We performed regressions (standard as wells as phylogenetically informed) to test if there were considerable deviations from isometry, and then calculated the ratios of eye/orbit diameter and pupil/orbit diameter, respectively, which we illustrated by histograms. To reproduce these figures, open the terminal in folders [figExt04_abcd](https://github.com/maciverlab/bigeye/tree/master/figs/figExt04abcd_orbit_eye) and [figExt04_efgh](https://github.com/maciverlab/bigeye/tree/master/figs/figExt04efgh_orbit_pupil) and run the following scripts…```$ Rscript figExt04_abcd.R --cwd$ Rscript figExt04_efgh.R --cwd
```

These will output and save the following figures:

![Eye orbit relationship]({{ site.url }}/assets/figExt_04abcd.png)

![Pupil orbit relationship]({{ site.url }}/assets/figExt_04efgh.png)


## Scaling of eye socket size in early tetrapods

It is well known that eyes become proportionately smaller with an increase of body size. As the early tetrapods in our study feature quite disparate body sizes we need to account for these scaling effects. Figure S5 illustrates our efforts in this regard. We ran this over our entire set of trees.

In all cases, early tetrapods featured negative allometry of eye sockets compared to skull length. Trying to remove the scaling effects by dividing eye socket size by skull length therefore doesn’t remove this size bias, but calculating residuals successfully removed scaling effects. To run our code, open the terminal in folder [figExt_05](https://github.com/maciverlab/bigeye/tree/master/figs/figExt05_scaling) and type…```$ Rscript figExt_05.R --cwd
```

These will output and save the following figure:

![Scaling of eye size]({{ site.url }}/assets/figExt05.png)

## Effect of different water models on visual range

Given that the actual intrinsic water properties and organic matter concentrations are not known for Late Devonian, we generated results for clear, absorption dominated, high turbidity and scattering dominated water types with details given in Supplementary Appendix Table S3. These have attenuation lengths of 1.17 m (clear), a high absorption water model at 0.52 m, a high turbidity model at 0.31 m, and a high scattering model at 0.22 m (quoted at 575 nm, the wavelength of highest transparency for the Baseline River water model used as our reference case).

The folder [aquatic_model](https://github.com/maciverlab/bigeye/tree/master/figs/figExt06_sensitivity/aquatic_model) contains the functions to calculate visual range based on both the firing and contrast threshold. *Aquatic_firingThreshSensitivity.m* calculates visual range based on firing threshold and saves it to the data file titled *meteoAquaticSensitivity.mat*, which contains both the pupil values used and a visual ranges (1st dimension across pupil diameters, 2nd dimension across water models and 3rd dimension across viewing directions). On the other hand, *Aquatic_contrastThreshSensitivity.m* loads the data file *meteoAquaticSensitivity.mat* and decreases range until the object is visible, which is dependent on the apparent contrast of the object and observer’s contrast threshold. These new ranges saved into a data file named *visibilityAquaticSensitivity.mat* while preserving the data structure. 

An example run of these two functions look like:

```Matlab
run Aquatic_firingThreshSensitivity
run Aquatic_contrastThreshSensitivity
```

These data files are then used to generate the main figure. The figure function can be found in [figures](https://github.com/maciverlab/bigeye/tree/master/figs/figExt06_sensitivity/figures) folder. Function titled *figExt06_sensitivity.m* takes in the optional boolean argument *CONTRASTTHRESH*, where the default value is set to be true. If specified as true, visual ranges based on contrast threshold will be plotted, and if false, visual ranges based on firing threshold will be displayed. Before creating the figure, the program searches for all of the required data files. If it any of them are missing the corresponding function is executed. If however all of the data files exist, the program asks the user if they want to re-generate the data. 


The figure function is executed by typing:

```Matlab
run figExt06_sensitivity
```

The output of this function is a two panel figure that depicts visual ranges based on different water models for upward and horizontal viewing.

![Visual range due to different water models]({{ site.url }}/assets/figExt06.png)


## Effect of object contrast on visual range

###  Contrast extraction from images


Various images of centipedes and millipedes in their native habitats were found through Google images, as well as a collection of freshwater underwater fish images from stills and videos. These images can be found by following instructions under the *Data* tab (navigation side bar). The colored images were converted to gray scale for pixel luminance values since the luminance of an image is calculated by the log-average luminance which converts colored images to grayscale. In the grayscale image the object (centipede, millipede, and fish) was user-identified by drawing a border around the desired target. The average luminance of the object (mean of the pixel values within the identified region) was calculated and the location was then masked. Similarly mean background luminance (all of the image minus the masked area) was calculated. Object contrast was calculated by subtracting mean background luminance from object luminance over object luminance (Weber contrast). The images are loaded and the object contrasts are calculated by executing the following Matlab command:


```Matlab
run getBugContrast
```


This function creates the data file *imageContrastValues.mat* that has contrast values for centipede and millipede under *bugContrast* array, fish contrast values under *fishContrast*, and image file locations under *fileNames*. These values are not explicitly used in the visual range calculations. But were used as a reference to find a possible range of naturalistic contrast values. 



### Visual range dependence on contrast


By definition the intrinsic contrast of an object can range from black (no reflection) (-1) to isoluminous with background (0), and then self-illuminating (> 0 to ∞). Contrast is important in determining the apparent luminance of the object (amount of light that reaches the eye from the object). Therefore, as the absolute value of the contrast decreases, the visual range based on firing threshold also decreases. On the other hand, it is easy to see that the apparent contrast of the object determines whether the object is visible (above the observer’s contrast threshold). 


We ran our computational model by fixing the pupil diameter (D) to finned and digited tetrapod pupil diameters, and varied contrast from -1 (black) to 4 (snow), for daylight in both aquatic and aerial conditions. 

The main folder [figExt07_contrast](https://github.com/maciverlab/bigeye/tree/master/figs/figExt07_contrast) has 4 folders which have the relevant codes for aerial model, aquatic model, contrast extraction from images and figure generation. 

In order to generate the figure simply type:

```Matlab
run figExt07_contrast
```

This code will output the following figure pdf:

![Contrast range relation for aquatic and aerial]({{ site.url }}/assets/figExt07.png) 

Similar to computational visual ecology code, each helper function can be executed to save calculated visual range data for one model. 

### Example run

If we take the aquatic model as an example run, the main folder that contains the relevant code is [aquatic_model](https://github.com/maciverlab/bigeye/tree/master/figs/figExt07_contrast/aquatic_model). Within this folder there is one function *Aquatic_daylightContrastRange.m* that calculates visual range for a set of contrast values and pupil diameters. Visual ranges are calculated, for both horizontal and upward viewing in daylight. The first part of the code calculates visual range based on firing threshold, and the second part decreases the range until the object becomes visible dependent on observer’s contrast threshold. Only one data file is created which has the range contrast values and pupil diameters, visual range values (where 1st dimension is across contrast, 2nd dimension is across pupil diameters, and 3rd dimension is across viewing). Unlike the computational visual code, the visual ranges calculated by using the simplified firing threshold model are not stored.


In order to execute the code type:


```Matlab
run Aquatic_daylightContrastRange.m
```

A similar execution can be done for the [aerial model](https://github.com/maciverlab/bigeye/tree/master/figs/figExt07_contrast/aerial_model) to get aerial daylight visual ranges under varying contrast. 

These will generate the required data files for both aquatic and aerial model. Functions to plot the created data files can be found under the [figures](https://github.com/maciverlab/bigeye/tree/master/figs/figExt07_contrast/figures) folder. Within it there is a main functions which generates the figure, and a helper function which interpolates visual range values to include isoluminous object (contrast of 0) by using the fact that  when the contrast of an object is 0 visual range is 0. 

Once the figure generation file *figExt07_contrast* is executed in Matlab, it will search through all the directories to see if the data files (*daylightVisibilityAerialContrast.mat* and *daylightVisibilityAquaticContrast.mat*) exist. If they do, the program will ask the user if they want to re-run all of the code and regenerate visual ranges. If however they do not, the program will run the corresponding function to the missing data file. Once the data files are available they will be loaded and the figure will be plotted and saved as pdf.  
