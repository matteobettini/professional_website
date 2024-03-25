---
title: "TorchRL: A data-driven decision-making library for PyTorch"
authors:
- Albert Bou
- admin
- Sebastian Dittert
- Vikash Kumar
- Shagun Sodhani
- Xiaomeng Yang
- Gianni De Fabritiis
- Vincent Moens

date: "2024-01-03T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *The Twelfth International Conference on Learning Representations (ICLR)* - __*Spotlight (top 5%)*__ 
publication_short: In *International Conference on Learning Representations (ICLR)* - __*Spotlight (top 5%)*__ 

abstract: Striking a balance between integration and modularity is crucial for a machine learning library to be versatile and user-friendly, especially in handling decision and control tasks that involve large development teams and complex, real-world data, and environments. To address this issue, we propose TorchRL, a generalistic control library for PyTorch that provides well-integrated, yet standalone components. With a versatile and robust primitive design, TorchRL facilitates streamlined algorithm development across the many branches of Reinforcement Learning (RL) and control. We introduce a new PyTorch primitive, TensorDict, as a flexible data carrier that empowers the integration of the library's components while preserving their modularity. Hence replay buffers, datasets, distributed data collectors, environments, transforms and objectives can be effortlessly used in isolation or combined. We provide a detailed description of the building blocks, supporting code examples and an extensive overview of the library across domains and tasks. Finally, we show comparative benchmarks to demonstrate its computational efficiency. TorchRL fosters long-term support and is publicly available on GitHub for greater reproducibility and collaboration within the research community. The code is opensourced [here](https://github.com/pytorch/rl).
# Summary. An optional shortened abstract.
summary: We propose TorchRL, a generalistic control library for PyTorch that provides well-integrated, yet standalone components. With a versatile and robust primitive design, TorchRL facilitates streamlined algorithm development across the many branches of Reinforcement Learning (RL) and control. We introduce a new PyTorch primitive, TensorDict, as a flexible data carrier that empowers the integration of the library’s components while preserving their modularity. TorchRL fosters long-term support and is publicly available on GitHub for greater reproducibility and collaboration within the research community.
  
tags:
- Multi-Agent Reinforcement Learning
featured: true

links:
- name: Documentation
  url: https://pytorch.org/rl/
- name: arXiv
  url: https://arxiv.org/abs/2306.00577
- name: OpenReview
  url: https://openreview.net/forum?id=QxItoEAVMb
  
url_pdf:
url_code: 'https://github.com/pytorch/rl'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'TorchRL rollout flow'
  placement: 1
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