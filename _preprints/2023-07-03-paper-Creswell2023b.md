---
title: "Understanding the impact of numerical solvers on inference for differential equation models"
collection: preprints
permalink: /preprint/Creswell2023b
excerpt: 'This paper investigates how numerical sovlers of differential equation models can affect their parameter inference'
date: 2023-07-03
venue: 'arXiv'
paperurl: 'http://arxiv.org/abs/2307.00749'
citation: 'Creswell, R., ..., Lei, C.L., Tavener, S., Robinson, M., and Gavaghan, D. (2020). &quot;Understanding the impact of numerical solvers on inference for differential equation models.&quot; <i>arXiv</i>.'
---
Most ordinary differential equation (ODE) models used to describe biological or physical systems must be solved approximately using numerical methods.
Perniciously, even those solvers which seem sufficiently accurate for the forward problem, i.e., for obtaining an accurate simulation, may not be sufficiently accurate for the inverse problem, i.e., for inferring the model parameters from data.
We show that for both fixed step and adaptive step ODE solvers, solving the forward problem with insufficient accuracy can distort likelihood surfaces, which may become jagged, causing inference algorithms to get stuck in local "phantom" optima.
We demonstrate that biases in inference arising from numerical approximation of ODEs are potentially most severe in systems involving low noise and rapid nonlinear dynamics.
We reanalyze an ODE changepoint model previously fit to the COVID-19 outbreak in Germany and show the effect of the step size on simulation and inference results.
We then fit a more complicated rainfall-runoff model to hydrological data and illustrate the importance of tuning solver tolerances to avoid distorted likelihood surfaces.
Our results indicate that when performing inference for ODE model parameters, adaptive step size solver tolerances must be set cautiously and likelihood surfaces should be inspected for characteristic signs of numerical issues.

[Download paper here](http://chonlei.github.io/files/Creswell2023b.pdf). Or [view here](http://arxiv.org/abs/2307.00749).
