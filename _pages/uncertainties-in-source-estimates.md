---
title: "Uncertainties in source estimates"
layout: page
date: 2016-03-23T11:48:41-04:00
image:
  feature: fake-feature.png
---

> We rely on inferences of subsurface fault slip to provide important insights after major earthquakes. More generally, we often use these images to explore the physics of the seismic source as well as post-seismic phenomena. We thus need these inferred images to be as accurate as possible, but we also need to be able to describe their limits, as well as the limits of the interpretations we derive from them.
>
> My research mainly focuses on the impact of an inaccurate description of the Earth s interior on source estimates. I focus on the effect of fault geometry, 3D crustal structure, and topography, and show that accounting for imperfect descriptions systematically increases the reliability of source estimates.

<figure>
  <img src="/images/research/unc2.png" alt="">
  <figcaption>Fig 1. Illustration of uncertainties affecting earthquake source estimates.</figcaption>
</figure>

Source estimates are constrained by the quality and quantity of observations, but are also severely impacted by the way we build the forward model and by any other prior information we include in the problem. Many authors have demonstrated that any change in the characteristics of the forward model (which include source parameterization but also description of the Earth's interior) may lead to variations in the inferred source properties. Yet, our understanding of Earth's interior structure will always remain uncertain, and thus will always be susceptible to include biases in inferred source properties.

One obvious way to limit the biases deriving from our imperfect description of the Earth is to make the description as close as possible to the reality. Another way to limit the biases deriving from our model approximations is to explicitly account for their imperfections. We build on this latter approach to account for uncertainties in fault geometry and crustal structure. We also investigate whether overlooking topography and post-seismic deformation can have a significant impact of coseismic slip estimates.

#### Fault geometry

Ragon et al., **2019**. Accounting for fault geometry uncertainty in source inversion --  II: Application to the 2016 Mw6.2 Amatrice earthquake. *Geophysical Journal International*, 218(1), 689–707, doi: [10.1093/gji/ggz180](https://doi.org/10.1093/gji/ggz180)  
Ragon et al., **2018**. Accounting for fault geometry uncertainty in source inversion --  I: theory and simplified application. *Geophysical Journal International*, 214(2), 1174-1190. doi: [10.1093/gji/ggy187](http://dx.doi.org/10.1093/gji/ggy187)  
{: .notice} 

The superficial geometry of seismic faults can be well observed when the seismic rupture reaches the surface. At depth, the real morphology of seismic faults is partially unknown, mainly because our observations are limited to the ground surface.
When solving for the characteristics of the seismic source, such as the slip distribution, we generally choose a particular fault geometry and assume this structure is undoubtedly realistic.

<figure>
  <img src="/images/research/unc3.png" alt="">
  <figcaption>Fig 2. Accounting for uncertainties in fault geometry: illustration for a simple 2D toy model.</figcaption>
</figure>

In Ragon et al. (2018), we proposed a methodology to account for uncertainties in the fault geometry. Based on a sensitivity analysis, this methodology incorporates the uncertainties of our approximations on the morphology of seismic faults in the inversion process. For both optimization approaches and probabilistic sampling methods, accounting for uncertainties in the fault geometry allows to reliably infer source characteristics even if our assumption on the fault geometry is incorrect.

The impact of fault geometry uncertainties on inferred models will depend on several parameters: sensibility of the observations to variations of the fault geometry, distribution of the observations, complexity of the fault geometry, degree of approximation of the fault morphology, etc. For most earthquakes, the impact of these uncertainties on the solution will thus be particularly difficult to anticipate. Yet, accounting for fault geometry uncertainties in the inversion process will be particularly significant for earthquakes with near fault observations, such as continental events.

#### Crustal Structure

Ragon et al., **2020**. Accounting for uncertain 3D elastic structure in fault slip estimates. *Geophysical Journal International*.  
Ragon et al., **2019**. Accounting for fault geometry uncertainty in source inversion --  II: Application to the 2016 Mw6.2 Amatrice earthquake. *Geophysical Journal International*, 218(1), 689–707, doi: [10.1093/gji/ggz180](https://doi.org/10.1093/gji/ggz180)
{: .notice} 

<figure>
  <img src="/images/research/unc4.png" alt="">
  <figcaption>Fig 3. Accounting for uncertainties in fault geometry and crustal structure: illustration for a simple 2D toy model.</figcaption>
</figure>

The fault geometry is not the only uncertain approximation we assume when we solve for the source characteristics. The crustal structure is often reduced to an homogeneous and elastic, or layered, medium. Yet, this approximations can have a large impact on inferred source models ( Beresnev 2003; Hartzell et al. 2007; Diao et al. 2016). We also show in Ragon et al. 2019 that all first-order uncertainties of the forward model must be accounted for to infer reliable models.

3D crustal heterogeneity is known to largely affect estimates of the seismic source and is usually overlooked. We also show in Ragon et al. (2020) that accounting for uncertainties in 3D crustal structure systematically increases the reliability of source estimates.

#### Topography 

Ragon, Langer et al., **2020**. Impact of topography on static slip estimates. *Tectonophysics*. [![preprint]({{ site.url }}/images/arxiv.png)](https://doi.org/10.31223/osf.io/nsbx3)
{: .notice} 

When solving for subsurface fault slip, it is common practice to assume minimum complexity for the Earth's characteristics such as topography, fault geometry and elastic properties. Yet, topography and bathymetry can be measured directly and are well known all over the Earth's surface. Accounting for topography thus seems to be an efficient strategy for incorporating accurate and extensive information into the inverse problem.

In Ragon, Langer et al. (2020), we show that topography has a non-negligible impact on inferred slip models. Our results suggest that the effect of topography on slip estimates increases with two main factors: limited observational constraints and high elevation gradients. In particular, we find that accounting for topography improves slip resolution where topographic gradients are large and the data is less informative: at depths for the Gorkha event, and near the trench for the Maule event. When topography has a significant impact on slip resolution, which is probably the case of many subduction events, the receiver elevation correction is not sufficient.

#### Early afterslip

Find more about early afterslip and how it impacts coseismic estimates [here](https://thearagon.github.io/thearagon.github.io/_pages/afterslip/).

<br style="line-height: 10px" />

##### A selected bibliography on uncertainties of the forward model:
- Beresnev, I. A., 2003. Uncertainties in Finite-Fault Slip Inversions: To What Extent to Believe? (A Critical Review), Bulletin of the Seismological Society of America, 93(6), 2445–2458.
- Hallo, M. & Gallovic, F., 2016. Fast and cheap approximation of Green function uncertainty for waveform-based earthquake source inversions, Geophysical Journal International, 207(2), 1012–1029.
- Hartzell, S., Liu, P., Mendoza, C., Ji, C., & Larson, K. M., 2007. Stability and Uncertainty of Finite-Fault Slip Inversions: Application to the 2004 Parkfield, California, Earthquake, Bulletin of the Seismological Society of America, 97(6), 1911–1934.
- Diao, F., Wang, R., Aochi, H., Walter, T. R., Zhang, Y., Zheng, Y., & Xiong, X., 2016. Rapid kinematic finite-fault inversion for an Mw 7+ scenario earthquake in the Marmara Sea: an uncertainty study, Geophysical Journal International, 204(2), 813–824.
- Duputel, Z., Rivera, L., Fukahata, Y., & Kanamori, H., 2012. Uncertainty estimations for seismic source inversions, Geophysical Journal International, 190(2), 1243–1256.
- Duputel, Z., Agram, P. S., Simons, M., Minson, S. E., & Beck, J. L., 2014. Accounting for prediction uncertainty when inferring subsurface fault slip, Geophysical journal international, 197(1), 464–482.
- Razafindrakoto, H. N. T. & Mai, P. M., 2014. Uncertainty in Earthquake Source Imaging Due to Variations in Source Time Function and Earth StructureUncertainty in Earthquake Source Imaging Due to Variations in Source Time Function and Earth Structure, Bulletin of the Seismological Society of America, 104(2), 855–874.
- Yagi, Y. & Fukahata, Y., 2011. Introduction of uncertainty of Green’s function into waveform inversion for seismic source processes, Geophysical Journal International, 186(2), 711–720.
{: .notice} 