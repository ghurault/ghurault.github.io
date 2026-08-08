---
title: "Making the most of eczema data for prediction, inference and treatment recommendation"

event_name: "Towards the future of AI"
event_url: "https://www.eventbrite.co.uk/e/towards-the-future-of-ai-tickets-329494405637"
location: "Imperial College London"
address:
  street: "South Kensington Campus"
  city: "London"
  country: "United Kingdom"

abstract: |
  **Background**: Atopic dermatitis (AD, eczema) is a chronic inflammatory skin disease with complex mechanisms that are not fully understood yet.
  Personalised eczema treatment recommendation is of high clinical relevance given the difficulties in predicting heterogeneous treatment responses.

  **Objective**: We aim to develop a comprehensive model that predicts the patient-dependent dynamic evolution of eczema severity and generates treatment recommendations.

  **Methods**: We introduced EczemaPred, a computational framework to predict the patient-dependent dynamic evolution of eczema severity using Bayesian state-space models that describe the latent dynamics of eczema severity and measurement errors.
  We used EczemaPred to predict nine eczema severity items, whose predictions were combined to produce predictions for PO-SCORAD, a validated self-assessed eczema severity score.
  We further extended EczemaPred to integrate data on treatment usage, estimate treatment effects, and generate treatment recommendations using Bayesian decision analysis.
  We also improved the quality of the training data by calibrating eczema severity recorded daily by patients with eczema severity assessed monthly by clinicians, and leveraged historical data to kickstart the training of the model and reach more robust conclusions.

  **Results**: EczemaPred achieved good performance in predicting PO-SCORAD and its severity items daily to weekly, and outperformed standard time-series forecasting models.
  Estimated treatment responses strongly depended on the patient’s clinical phenotype and allowed us to generate patient-specific treatment recommendations.
  EczemaPred is available as an [R package](https://ghurault.github.io/EczemaPred/).

# Talk start and end times.
date: 2022-06-07T13:00:00+01:00
event_start: 2022-06-07T13:00:00+01:00
event_end: 2022-06-07T17:00:00+01:00
event_all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2022-06-06T11:19:33+01:00

authors: ["admin"]
tags: ["poster", "eczema"]

featured: false

links:
  - type: poster
    url: uploads/2022_TFAI_Poster.pdf
---
