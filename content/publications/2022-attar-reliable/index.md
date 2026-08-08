---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Reliable detection of eczema areas for fully automated assessment of eczema severity from digital camera images"
authors: ["R. Attar", "admin", "Z. Wang", "R. Mokhtari", "K. Pan", "B. Olabi", "E. Earp", "L. Steele", "H. C. Williams", "R. J. Tanaka"]
date: 2023-07-18
doi: "10.1016/j.xjidi.2023.100213"

# Schedule page publish date (NOT publication's date).
publishDate: 2022-11-07

# Publication type.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "JID Innovations"
publication_short: "JID Innovations"

abstract: "
Assessing the severity of eczema in clinical research requires face-to-face skin examination by trained staff. Such approaches are resource-intensive for participants and staff, challenging during pandemics, and prone to inter- and intra-observer variation. Computer vision algorithms have been proposed to automate the assessment of eczema severity using digital camera images. However, they often require human intervention to detect eczema lesions and cannot automatically assess eczema severity from real-world images in an end-to-end pipeline. We developed a model to detect eczema lesions from images using data augmentation and pixel-level segmentation of eczema lesions on 1345 images provided by dermatologists. We evaluated the quality of the obtained segmentation compared to that of the clinicians, the robustness to varying imaging conditions encountered in real-life images, such as lighting, focus, and blur and the performance of downstream severity prediction when using the detected eczema lesions. The quality and robustness of eczema lesion detection increased by approximately 25% and 40%, respectively, compared to our previous eczema detection model. The performance of the downstream severity prediction remained unchanged. Use of skin segmentation as an alternative to eczema segmentation that requires specialist labelling showed the performance on par with when eczema segmentation is used.
"

# Summary. An optional shortened abstract.
summary: ""

tags: ["Atopic dermatitis", "severity scores", "deep neural networks", "fully automated image analysis", "automated remote assessment", "robustness"]
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: MedRxiv
  url: "https://doi.org/10.1101/2022.11.05.22281951"

url_pdf:
url_code: "https://github.com/Tanaka-Group/EczemaNet2"
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
