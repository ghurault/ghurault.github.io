---
title: "Detecting eczema areas in digital images: an impossible task?"
authors: ["admin", "K. Pan", "R. Mokhtari", "B. Olabi", "E. Earp", "L. Steele", "H. C. Williams", "R. J. Tanaka"]
date: 2022-03-09

# Schedule page publish date (NOT publication's date).
publishDate: 2022-03-09

# Publication type, from the CSL standard.
publication_types: ["article-journal"]

publication:
  name: "JID Innovations"
  volume: 2
  issue: 5
  pages: "100133"

abstract: "
Assessing the severity of atopic dermatitis (AD, or eczema) traditionally relies on a face-to-face assessment by healthcare professionals, and may suffer from inter- and intra-rater variability.
With the expanding role of telemedicine, several machine learning algorithms have been proposed to automatically assess AD severity from digital images.
Those algorithms usually detect and then delineate (“segment”) AD lesions before assessing lesional severity, and are trained using the data of AD areas detected by healthcare professionals.
To evaluate the reliability of such data, we estimated the inter-rater reliability of AD segmentation in digital images.

Four dermatologists independently segmented AD lesions in 80 digital images collected in a published clinical trial.
We estimated the inter-rater reliability of the AD segmentation using the intra-class correlation coefficients (ICCs) at the pixel-level and the area-levels for different resolutions of the images.
The average ICC was 0.45 (SE=0.04) corresponding to a “poor” agreement between raters, while the degree of agreement for AD segmentation varied from image to image.

The AD segmentation in digital images is highly rater-dependent even between dermatologists.
Such limitations need to be taken into consideration when the AD segmentation data are used to train machine learning algorithms that assess eczema severity.
"

# Summary. An optional shortened abstract.
summary: ""

tags: []
featured: true

hugoblox:
  ids:
    doi: 10.1016/j.xjidi.2022.100133

links:
  - type: code
    url: "https://github.com/ghurault/IRR-eczema-images"
  - type: preprint
    url: "https://doi.org/10.1101/2022.03.03.22271780"
    label: medRxiv
---
