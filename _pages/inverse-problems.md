---
title: "Bayesian sampling"
layout: page
date: 2016-03-23T11:48:41-04:00
image:
  feature: fake-feature.png
---

> Using Bayesian methods allow us to infer the distribution of the parameters of most probable models, and thus to estimate the posterior uncertainty of inferred parameters. Additionally, no prior spatial smoothing (that can lead to spurious effects in inferred models) is needed to restrain the exploration of the solution space.

The ill-posed nature of earthquake source estimation derives from several factors including data quality, quantity and processing (filtering, sampling, etc.) that controls the level of information available to reduce the uniqueness of the problem. Other factors affecting estimates of the source are related to our simplified description of the physics of the problem, which is inherently more difficult to quantify. Source parametrization and the inversion method will both affect our estimates of source characteristics. In particular, any simplification including the possible linearization of the inverse problem, the level of complexity in the discretization of the source, smoothing and other types of regularization will impact the solutions of the inverse problem (e.g. Du et al. 1992; Beresnev 2003). Our imperfect forward problem can produce systematic errors and biases (more details here).

When trying to estimate source processes, inferred models can thus be very discrepant while explaining the observations equally well. When looking for the best model of the solution space, we could thus overlook another almost-best model. And which one could be the more realistic?
Additionally, the uncertainties in the observations and in our assumed forward model necessarily implies that our inferred model is uncertain. What are the uncertainties of our results?

<figure>
  <img src="/images/research/inv1.png" alt="">
  <figcaption>Fig 1.  Bayesian sampling methods allow us to explore plausible solutions.</figcaption>
</figure>
{: .align-center}

Instead of trying to infer the best model, we could explore the distribution of the most probable models (Tarantola & Valette, 1982; Mosegaard & Tarantola, 1995). To do so, we need to estimate the likelihood of a particular model based on available observations. This estimation is possible thanks to the Bayes theorem, which indicates that the likelihood of a model can be derived from its probability to explain the observations and from prior information on the model.

Using Bayesian methods allow us to infer the distribution of the parameters of most probable models, and thus to estimate the posterior uncertainty of inferred parameters. Additionally, no prior spatial smoothing (that can lead to spurious effects in inferred models, according to Beresnev et al. 2003; Causse et al., 2010; Gallovič et al., 2015; Gombert et al., 2017) is needed to restrain the exploration of the solution space.

Each inferred parameter is defined by its Probability Density Function (PDF). Inferred parameters can thus be described by the mean, the median, the maximum a posteriori of the PDF along with the posterior uncertainty (standard deviation of the PDF, that is often Gaussian-shaped). Another option is to [classify the explored solution space into characteristic families](https://thearagon.github.io/thearagon.github.io/_pages/vizualization-of-uncertainties/).

<figure>
  <img src="/images/research/inv2.png" alt="">
  <figcaption>Fig 2. Comparison of two coseismic models inferred for the 2016 Mw 6.3 Amatrice earthquake, Italy. The two models solve for the same dataset with a similar forward model, expect for the fault geometry which is different.</figcaption>
</figure>
{: .align-center}

##### References
- Beresnev, I. A., 2003. Uncertainties in Finite-Fault Slip Inversions: To What Extent to Believe? (A Critical Review), Bulletin of the Seismological Society of America, 93(6), 2445–2458.
- Causse, M., Cotton, F., & Mai, P. M., 2010. Constraining the roughness degree of slip heterogeneity, Journal of Geophysical Research : Solid Earth, 115(B5).
- Du, Y., Aydin, A. & Segall, P., 1992. Comparison of various inversion techniques as applied to the determination of a geophysical deformation model for the 1983 Borah Peak earthquake, Bull. seism. Soc. Am., 82(4), 1840–1866.
- Gallovič, F., Imperatori, W., & Mai, P. M., 2015. Effects of three-dimensional crustal structure and smoothing constraint on earthquake slip inversions : Case study of the Mw6.3 2009 L’Aquila earthquake, Journal of Geophysical Research : Solid Earth, 120(1), 2014JB011650.
- Gombert, B., Duputel, Z., Jolivet, R., Doubre, C., Rivera, L., & Simons, M., 2017. Revisiting the 1992 Landers earthquake : A Bayesian exploration of co seismic slip and off-fault damage, Geophysical Journal International.
- Minson, S.E., Simons, M. & Beck, J.L., 2013. Bayesian inversion for finite fault earthquake source models I-theory and algorithm, Geophys. J. Int., 194(3), 1701–1726.
- Minson, S.E. et al., 2014. Bayesian inversion for finite fault earthquake source models – II: the 2011 great Tohoku-Oki, Japan earthquake, Geophys. J. Int., 198(2), 922–940.
- Mosegaard, K. & Tarantola, A., 1995. Monte Carlo sampling of solutions to inverse problems, Journal of Geophysical Research : Solid Earth, 100(B7), 12431–12447.
- Tarantola, A., 2005. Inverse Problem Theory and Methods for Model Parameter Estimation, Other Titles in Applied Mathematics, Society for Industrial and Applied Mathematics.
- Tarantola, A. & Valette, B., 1982. Generalized nonlinear inverse problems solved using the least squares criterion, Reviews of Geophysics, 20(2), 219–232.
{: .notice} 