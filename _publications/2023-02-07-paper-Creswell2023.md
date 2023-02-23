---
title: "A Bayesian nonparametric method for detecting rapid changes in disease transmission"
collection: publications
permalink: /publication/Creswell2023
excerpt: 'This paper introduces a Bayesian nonparametric way to detect changes in disease transmission, applying to various real-world data including COVID-19.'
date: 2023-02-07
venue: 'Journal of Theoretical Biology'
paperurl: 'https://doi.org/10.1016/j.jtbi.2022.111351'
citation: 'Creswell, R., ..., Lei, C.L. and Lambert, B. (2023). &quot;A Bayesian nonparametric method for detecting rapid changes in disease transmission.&quot; <i>Journal of Theoretical Biology</i>, 558, 111351.'
---
Whether an outbreak of infectious disease is likely to grow or dissipate is determined through the time-varying reproduction number, Rt.
Real-time or retrospective identification of changes in Rt following the imposition or relaxation of interventions can thus contribute important evidence about disease transmission dynamics which can inform policymaking.
Here, we present a method for estimating shifts in Rt within a renewal model framework.
Our method, which we call EpiCluster, is a Bayesian nonparametric model based on the Pitman–Yor process.
We assume that Rt is piecewise-constant, and the incidence data and priors determine when or whether Rt should change and how many times it should do so throughout the series.
We also introduce a prior which induces sparsity over the number of changepoints. Being Bayesian, our approach yields a measure of uncertainty in Rt and its changepoints.
EpiCluster is fast, straightforward to use, and we demonstrate that it provides automated detection of rapid changes in transmission, either in real-time or retrospectively, for synthetic data series where the Rt profile is known.
We illustrate the practical utility of our method by fitting it to case data of outbreaks of COVID-19 in Australia and Hong Kong, where it finds changepoints coinciding with the imposition of non-pharmaceutical interventions.
Bayesian nonparametric methods, such as ours, allow the volume and complexity of the data to dictate the number of parameters required to approximate the process and should find wide application in epidemiology.

[Download paper here](http://chonlei.github.io/files/Creswell2023.pdf). Or [view here](https://doi.org/10.1016/j.jtbi.2022.111351).
