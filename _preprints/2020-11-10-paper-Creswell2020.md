---
title: "Using flexible noise models to avoid noise model misspecification in inference of differential equation time series models"
collection: preprints
permalink: /preprint/Creswell2020
excerpt: 'This paper develops two flexible noise models handle unknown noise generating processes when performing inference of differential equation time series models.'
date: 2020-11-10
venue: 'arXiv'
paperurl: 'http://arxiv.org/abs/2011.04854'
citation: 'Creswell, R., Lambert, B., Lei, C.L., Robinson, M., & Gavaghan, D. (2020). &quot;Using flexible noise models to avoid noise model misspecification in inference of differential equation time series models.&quot; <i>arXiv</i>.'
---
When modelling time series, it is common to decompose observed variation into a "signal" process, the process of interest, and "noise", representing nuisance factors that obfuscate the signal.
To separate signal from noise, assumptions must be made about both parts of the system.
If the signal process is incorrectly specified, our predictions using this model may generalise poorly;
similarly, if the noise process is incorrectly specified, we can attribute too much or too little observed variation to the signal.
With little justification, independent Gaussian noise is typically chosen, which defines a statistical model that is simple to implement but often misstates system uncertainty and may underestimate error autocorrelation.
There are a range of alternative noise processes available but, in practice, none of these may be entirely appropriate, as actual noise may be better characterised as a time-varying mixture of these various types.
Here, we consider systems where the signal is modelled with ordinary differential equations and present classes of flexible noise processes that adapt to a system's characteristics.
Our noise models include a multivariate normal kernel where Gaussian processes allow for non-stationary persistence and variance, and nonparametric Bayesian models that partition time series into distinct blocks of separate noise structures.
Across the scenarios we consider, these noise processes faithfully reproduce true system uncertainty: that is, parameter estimate uncertainty when doing inference using the correct noise model.
The models themselves and the methods for fitting them are scalable to large datasets and could help to ensure more appropriate quantification of uncertainty in a host of time series models.

[Download paper here](http://chonlei.github.io/files/Creswell2020.pdf). Or [view here](http://arxiv.org/abs/2011.04854).
