# JSMM

Joint species movement model (JSMM) R-code, instructions on how to use it and input data from the manuscript Otso Ovaskainen, Danielle Leal Ramos, Marco Aurélio Pizo, Milton Cezar Ribeiro and Juan Manuel Morales. Joint species movement modeling: how do species´ traits influence their movements?

Abstract. Recent advances in joint species distribution modeling (JSDM) have enabled researchers to move from species-level analyses to community-level analyses, leading to statistically more efficient and ecologically more informative use of data. Here we propose joint species movement modeling (JSMM) as an analogous approach that enables one to infer both species- and community-level movement parameters from multi-species capture-recapture data. The species-level movement parameters are modeled as a function of species traits and/or their phylogenetic relationships, allowing one to ask how species traits influence movements, and whether phylogenetically related species are more similar in their movement patterns than expected based on the measured traits. We illustrate the performance of the modeling framework with data on bird movement in a heterogeneous landscape in Brazil. The results show that, in our data, both affinity to forests (compared to pastures) as well as movement distances increase with the body size of the species, and that movement behavior varies among birds belonging to different feeding types. As expected, the JSMM approach improved species-specific movement parameters especially for those species with limited data. The JSMM model passed a strong test of structural model validation in the sense that it generated simulated movement data that were indistinguishable from real data to bird experts who attempted to score movement patterns either as real or as simulated. Our results demonstrate that joint species movement modeling provides a statistically efficient framework for analyzing multi-species movement data, facilitating a synthetic understanding of the causes and consequences of variation in movement behavior across species.

We provide here the code for the JSMM (JSMM.Rmd), which consists mainly of one likelihood function and a MCMC sampling scheme with a Metropolis-Hastings step. We also provide a dataset on bird movement in a heterogeneous landscape in Brazil to demonstrate the model – the sequence of movement steps of 43 bird species, their traits and phylogenetic relationship, and the landscape covariates. The code estimates the movement parameters posteriors and their convergence, and produces a figure to show the influence of species traits on species-specific parameters.
The JSMM can be used for many kinds of movement models and movement data by adapting the likelihood function, which should use 3 inputs: the species movement data, the environmental covariates, and the parameters to be sampled. We illustrate it with a simple step-selection model.
