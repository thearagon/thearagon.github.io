---
title: "Vizualizing uncertainties"
layout: page
date: 2016-03-23T11:48:41-04:00
image:
  feature: fake-feature.png
---

> My research often relies on the interpretation of uncertain data or estimates. This uncertainty can sometimes derive from the variability of multiple plausible models. For instance, an usual Bayesian sampling approach will yield more than 150.000 possible models. How do we represent the full range of possibilities? How do we highlight most probable models while revealing their characteristic features and inherent uncertainties?

We usually vizualize results of Bayesian estimates using a simple mean and standard deviation representation, or representing the posterior probability density functions. These approaches have several drawbacks if the number of model parameters is large and can be spatially correlated. Indeed, these vizualization approaches do not allow to show spatial correlation between parameters of a particular sample, or within a set of samples, and do not allow either to intuitively grasp the uncertainties in every parameter.

I am developing several approaches to improve our vizualization of such estimates. A first approach consists in grouping samples into characteristic families. A second one makes use of [value-suppressing uncertainty palettes](https://medium.com/@uwdata/value-suppressing-uncertainty-palettes-426130122ce9).

#### Families of models

Ragon et al, **2019**. Joint inversion of co-seismic and early post-seismic slip to optimize the information content in geodetic data: application to the 2009 Mw6.3 L'Aquila earthquake, Central Italy. *JGR Solid Earth*, doi: [10.1029/2018JB017053](https://doi.org/10.1029/2018JB017053). 
Ragon et al., **2019**. Accounting for fault geometry uncertainty in source inversion --  II: Application to the 2016 Mw6.2 Amatrice earthquake. *Geophysical Journal International*, 218(1), 689–707, doi: [10.1093/gji/ggz180](https://doi.org/10.1093/gji/ggz180)  
{: .notice} 

We can group inferred models in several families of models. Each family can then be represented by its median model. Or we could also randomly select a model in each of the families. These illustrations allow us to easily and intuitively decipher the posterior uncertainty of each parameter, the spatial correlation between the parameters (trade-off) and the area of high slip amplitudes.

<figure>
  <img src="/images/research/viz2.gif" alt="">
  <figcaption>Fig 1. Illustration of uncertainties affecting earthquake source estimates.</figcaption>
</figure>


