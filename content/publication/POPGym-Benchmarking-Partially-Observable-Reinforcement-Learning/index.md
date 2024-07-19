---
title: "POPGym: Benchmarking Partially Observable Reinforcement Learning"
authors:
- morad
- kortvelesy
- admin
- Stephan Liwicki
- prorok
date: "2023-01-04T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *International Conference on Learning Representations (ICLR)*
publication_short: In *International Conference on Learning Representations (ICLR)*

abstract: Real world applications of Reinforcement Learning (RL) are often partially observable, thus requiring memory. Despite this, partial observability is still largely ignored by contemporary RL benchmarks and libraries. We introduce Partially Observable Process Gym (POPGym), a two-part library containing (1) a diverse collection of 14 partially observable environments, each with multiple difficulties and (2) implementations of 13 memory model baselines – the most in a single RL library. Existing partially observable benchmarks tend to fixate on 3D visual navigation, which is computationally expensive and only one type of many possible POMDPs. In contrast, POPGym environments are diverse, produce smaller observations, use less memory, and often converge within two hours of training on a consumer-grade GPU. We implement our high-level memory API and memory baselines on top of the popular RLlib framework, providing plug-and-play compatibility with various training algorithms, exploration strategies, and distributed training paradigms. Using POPGym, we execute the largest comparison across RL memory models to date.
# Summary. An optional shortened abstract.
summary: We introduce Partially Observable Process Gym (POPGym), a two-part library containing (1) a diverse collection of 14 partially observable environments, each with multiple difficulties and (2) implementations of 13 memory model baselines – the most in a single RL library. Using POPGym, we execute the largest comparison across RL memory models to date. 

tags:
  - Software library

featured: false

links:
- name: arXiv
  url: https://arxiv.org/abs/2303.01859
- name: OpenReview
  url: https://openreview.net/forum?id=chDrutUTs0K
- name: Poster
  url: poster.png
url_pdf:
url_code: 'https://github.com/smorad/popgym'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  placement: 2
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