---
title: Generating the summary of our phylogenetic comparative study
paper: bigeye
categories: bigeye
---

You can visualize the main results of our phylogenetic comparative analysis (similar to Fig. 2) by executing the code in folder [fig02_phylo_orbit](https://github.com/maciverlab/bigeye/tree/master/figs/fig02_phylo_orbit) in the project GitHub. The script plots the phylogeny of the species in our analysis, scaled against geologic time, and illustrates the residual eye socket size of early tetrapods by adding scaled dots to the tips. It also highlights the branches along which we found support for changes in the selective regime of eye socket evolution. These branches were identified with bayou, an R package for characterizing the dynamics of adaptive landscape. Note that we are summarizing results over a set of 1000 trees. The major differences between the trees concern the time-scaling, and the topology of three unresolved parts of the tree. These polytomies were resolved randomly and branches in these parts of the tree did not feature well-supported shifts in eye socket size evolution.To run the code, go to the directory of the script in terminal/command prompt and type…

```
$ Rscript fig02.R --cwd
```

This script will output the following figure (saved as pdf):


![Summary of our phylogenetic comparative study]({{ site.url }}/assets/fig02.png)


## Full phylogenetic comparative analysis

If you would like to run the full phylogenetic comparative analysis with the same settings that we used for the paper, you can run the code in folder ‘bayou’. Depending on your computer the script may run for a few days. Open the terminal in the bayou folder to initiate the analysis…```$ Rscript bayou_parallel_BM.R --cwd
```

The results will be saved at the end of the run in the bayou folder. You can change the settings of the analysis by modifying the original R code; please let us know if we can help with that. If you would like to run the analysis with residuals obtained from regression in an Ornstein-Uhlenbeck framework (as opposed to Brownian motion), you can run this script:```
$ Rscript bayou_parallel_OU.R --cwd```

## Diagnostic tests

We performed several diagnostic tests to ensure that convergence of the two reversible jump mcmc chains was achieved, which are shown in the Supplementary Appendix Figure S3. One such characteristic is Gelman’s R, which we calculated for logLikelihood, alpha, and sigma^2. You can reproduce an example of this by executing the code in folder [fig03Ext_abc](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03abc_gelman). Open the terminal in that folder and type this command…```$ Rscript figExt03_abc.R --cwd
```![Gelmans R]({{ site.url }}/assets/figExt_03abc.png)


The fourth panel of this plot shows a bivariate plot of the posterior probabilities of a selective regime shift along a branch from both chains. If convergence is achieved, the dots should fall roughly along a line. In the figure below, we have summarized the posterior probabilities from both chains for all branches across all trees. To make the plot more legible, we shaded the high density areas instead of plotting every single point. Open the terminal in folder [figExt03_d](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03d_PP) to run the script…

```$ Rscript figExt03_d.R --cwd
```

![Posterior probabilities]({{ site.url }}/assets/figExt_03d.png)

To further visualize bayou results we provide scripts to plot frequency distribution of posterior probabilities of rate shifts along branches and the estimated peak eye socket sizes for selected branches in folders [figExt03e_freq](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03e_freq) and [figExt03_f_peaks](https://github.com/maciverlab/bigeye/tree/master/figs/figExt03f_peaks).
