---
title: "EczemaPred: A computational framework for personalised prediction of eczema severity dynamics"
authors: ["admin", "J-F. Stalder", "S. Mery", "A. Delarue", "M. Saint Aroman", "G. Josse", "R. J. Tanaka"]
date: 2022-03-28

# Schedule page publish date (NOT publication's date).
publishDate: 2022-03-15

# Publication type, from the CSL standard.
publication_types: ["article-journal"]

publication:
  name: "Clinical and Translational Allergy"
  volume: 12
  issue: 3
  pages: "e12140"

abstract: "
**Background**: Atopic dermatitis (AD) is a chronic inflammatory skin disease leading to substantial quality of life impairment with heterogeneous treatment responses.
People with AD would benefit from personalised treatment strategies, whose design requires predicting how AD severity evolves for each individual.
**Objective**: This study aims to develop a computational framework for personalised prediction of AD severity dynamics.
**Methods**: We introduced EczemaPred, a computational framework to predict patient-dependent dynamic evolution of AD severity using Bayesian state-space models that describe latent dynamics of AD severity items and how they are measured.
We used EczemaPred to predict the dynamic evolution of validated patient-oriented scoring atopic dermatitis (PO-SCORAD) by combining predictions from the models for the nine severity items of PO-SCORAD (six intensity signs, extent of eczema, and two subjective symptoms).
We validated this approach using longitudinal data from two independent studies: a published clinical study in which PO-SCORAD was measured twice weekly for 347 AD patients over 17 weeks, and another one in which PO-SCORAD was recorded daily by 16 AD patients for 12 weeks.
**Results**: EczemaPred achieved good performance for personalised predictions of PO-SCORAD and its severity items daily to weekly.
EczemaPred outperformed standard time-series forecasting models such as a mixed effect autoregressive model.
The uncertainty in predicting PO-SCORAD was mainly attributed to that in predicting intensity signs (75% of the overall uncertainty).
**Conclusions**: EczemaPred serves as a computational framework to make a personalised prediction of AD severity dynamics relevant to clinical practice.
EczemaPred is available as an R package.
"

# Summary. An optional shortened abstract.
summary: "Prediction of the patient-specific dynamic evolution of AD severity by EczemaPred will help manage and anticipate fluctuating disease symptoms, contributing to personalised medicine."

tags: ["atopic dermatitis", "bayesian model", "machine learning", "po-scorad", "prediction"]
featured: true

hugoblox:
  ids:
    doi: 10.1002/clt2.12140

links:
  - type: code
    url: "https://github.com/ghurault/EczemaPred"
    label: R package
  - type: code
    url: "https://github.com/ghurault/EczemaPredPOSCORAD"
    label: Analysis code
---
