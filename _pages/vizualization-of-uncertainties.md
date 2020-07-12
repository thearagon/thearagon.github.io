---
title: "Vizualizing uncertainties"
layout: page
date: 2016-03-23T11:48:41-04:00
image:
  feature: fake-feature.png
---

> My research often relies on the interpretation of uncertain data or estimates. This uncertainty can sometimes derive from the variability of multiple plausible models. For instance, an usual Bayesian sampling approach will yield more than 150.000 possible models. How do we represent the full range of possibilities? How do we highlight the most probable models while revealing their characteristic features and inherent uncertainties?

We usually vizualize results of Bayesian estimates using a simple mean and standard deviation representation, or representing the posterior probability density functions. These approaches have several drawbacks if the number of model parameters is large and if parameters can be spatially correlated. Indeed, these vizualization approaches do not allow to show spatial correlation between parameters of a particular sample, or within a set of samples, and do not allow either to intuitively grasp the uncertainties in every parameter.

I am developing several approaches to improve our vizualization of such estimates. A first approach consists in grouping samples into characteristic families. A second one makes use of [value-suppressing uncertainty palettes](https://medium.com/@uwdata/value-suppressing-uncertainty-palettes-426130122ce9).

#### Families of models

Ragon et al, **2019**. Joint inversion of co-seismic and early post-seismic slip to optimize the information content in geodetic data: application to the 2009 Mw6.3 L'Aquila earthquake, Central Italy. *JGR Solid Earth*, doi: [10.1029/2018JB017053](https://doi.org/10.1029/2018JB017053).  
Ragon et al., **2019**. Accounting for fault geometry uncertainty in source inversion --  II: Application to the 2016 Mw6.2 Amatrice earthquake. *Geophysical Journal International*, 218(1), 689–707, doi: [10.1093/gji/ggz180](https://doi.org/10.1093/gji/ggz180)  
{: .notice} 

We can group inferred models in several families of models. Each family can then be represented by its median model. Or we could also randomly select a model in each of the families. These illustrations allow us to easily and intuitively decipher the posterior uncertainty of each parameter, the spatial correlation between the parameters (trade-off) and the area of high slip amplitudes.

<figure>
  <img src="/images/research/viz2.gif" alt="">
  <figcaption>Fig 1. Animated co-seismic slip distribution for the 2016 Amatrice earthquake, Mw6.2, Central Italy. Random samples are selected in each family of models..</figcaption>
</figure>
{: .align-center}

##### How are the family of models built?
The set of samples inferred from an inversion is divided into 25 subsets, for simplicity. The families of models are chosen and built iteratively. Each sample is selected randomly, and included in a family:
- The first family gathers samples whose parameters are of less than 50 cm offset from the median model parameters. In detail, a model is added to the first family if the selected model and the median model are parameter-wise equal within a relative tolerance of 20\% added to an absolute tolerance of 50 cm.
- If the selected model doesn’t fall in the first family, it is used as root for the second family.
- The last family regroups orphan samples.  

The first family is the most populated, as around the median model, and gathers the most probable models. In contrast, other families group models with a smaller likelihood, but that may prove as realistic as the median model.
The threshold value (in this example of 50 cm) is adapted empirically so that the number of samples in each family is equivalent — except for the 1st family. This threshold usually corresponds to the standard deviation of peak slip amplitude parameters. 

Currently, a simple L2 norm residual is used to measure the distance between samples. Multiclass classification methods, mostly based on machine learning algorithms, could improve the classification.


#### Value-suppressing uncertainty palette

Unpublished yet.
{: .notice} 

A value-suppressing uncertainty palette is a bivariate palette (representing every combination of a value and its uncertainty) for which the number of represented combinations is gradually reduced with the uncertainty. You can find more detailed explanations in [this article](https://medium.com/@uwdata/value-suppressing-uncertainty-palettes-426130122ce9). 

<figure>
  <img src="/images/research/viz3.png" alt="">
  <figcaption>Fig 2. Coseismic model for the 2010 Mw 8.8 Maule earthquake, published in Ragon, Langer et al. (2020). </figcaption>
</figure>
{: .align-center}
