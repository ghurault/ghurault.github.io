---
title: "PhD project"
summary: "Towards a data-driven personalised management of Atopic Dermatitis severity."
authors: ["admin"]
date: 2022-06-01

# Clicking the card opens this URL directly, in place of a detail page.
external_link: "https://hdl.handle.net/10044/1/105985"

# Show the featured image in listings only, not on the page itself.
image:
  preview_only: true

hugoblox:
  ids:
    doi: 10.25560/105985
---

## Abstract

Atopic Dermatitis (AD, eczema) is a common inflammatory skin disease, characterised by dry and itchy skin.
AD cannot be cured, but its long-term outcomes can be managed with treatments.
Given the heterogeneity in patients' responses to treatment, designing personalised rather than "one-size-fits-all" treatment strategies is of high clinical relevance.
In this thesis, we aim to pave the way towards a data-driven personalised management of AD severity, whereby severity data would be collected automatically from photographs without the need for patients to visit a clinic, be used to predict the evolution of AD severity, and generate personalised treatment recommendations.

First, we developed EczemaNet[^2020-eczemanet], a computer vision pipeline using convolution neural networks that detects areas of AD from photographs and then makes probabilistic assessments of AD severity.
EczemaNet was internally validated with a medium-size dataset of images collected in a published clinical trial and demonstrated fair performance.

Then, we developed models predicting the daily to weekly evolution of AD severity[^2020-mechanistic-ml].
We highlighted the challenges of extracting signals from noisy severity data, with small and practically not significant effects of environmental factors[^2020-pollution] and biomarkers[^2020-ssm-biomarkers] on prediction.
We showed the importance of using high-quality measurements of validated and objective (vs subjective) severity scores.
We also stressed the importance of modelling individual severity items rather than aggregate scores, and introduced EczemaPred[^2022-eczemapred], a principled approach to predict AD severity using Bayesian state-space models.
Our models are flexible by design, interpretable and can quantify uncertainty in measurements, parameters and predictions.
The models demonstrated good performance to predict the Patient-Oriented SCOring AD (PO-SCORAD).

Finally, we generated personalised treatment recommendations using Bayesian decision analysis.
We observed that treatment effects and recommendations could be confounded by the clinical phenotype of patients.
We also pretrained our model using historical data and combined clinical and self-assessments.

In conclusion, we have demonstrated the feasibility and the challenges of a data-driven personalised management of AD severity.

## References

[^2020-eczemanet]: [K. Pan,  **G. Hurault**, K. Arulkumaran, H. Williams and R. J. Tanaka,
"EczemaNet: Automating Detection and Assessment of Atopic Dermatitis",
*International Workshop on Machine Learning in Medical Imaging*, 2020](https://doi.org/10.1007/978-3-030-59861-7_23)

[^2020-mechanistic-ml]: [**G. Hurault**, E. Domínguez-Hüttinger, S. M. Langan, H. C. Williams and R. J. Tanaka,
"Personalised prediction of daily eczema severity scores using a mechanistic machine learning model",
*Clinical \& Experimental Allergy*, vol. 50, no. 11, pp. 1258–1266, 2020](https://doi.org/10.1111/cea.13717)

[^2020-ssm-biomarkers]: [**G. Hurault**, E. Roekevisch, M.E. Schram, K. Szegedi, S. Kezic, M.A. Middelkamp-Hup, P.I. Spuls and R. J. Tanaka,
"Can serum biomarkers predict the outcome of systemic immunosuppressive therapy in adult atopic dermatitis patients?",
*Skin and Health Disease*, vol. 2, no. 1, p. e77, 2022.](https://doi.org/10.1002/ski2.77)

[^2020-pollution]: [**G. Hurault**, V. Delorieux, Y-M. Kim, K. Ahn, H. Williams and R. J. Tanaka,
"Impact of environmental factors in predicting daily severity scores of atopic dermatitis",
*Clinical and Translational Allergy, vol. 11, no. 2*, 2021](https://doi.org/10.1002/clt2.12019)

[^2022-eczemapred]: [**G. Hurault**, J-F Stalder, S. Mery, A. Delarue, M. Saint Aroma, G. Josse and R. J. Tanaka,
"EczemaPred: A computational framework for personalised prediction of eczema severity dynamics",
*Clinical and Translational Allergy*, 2022, vol. 12, no. 3, p. e12140.](https://doi.org/10.1002/clt2.12140)
