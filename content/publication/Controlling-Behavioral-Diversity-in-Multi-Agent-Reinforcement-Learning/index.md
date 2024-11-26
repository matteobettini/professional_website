---
title: "Controlling Behavioral Diversity in Multi-Agent Reinforcement Learning"
authors:
- admin
- kortvelesy
- prorok

date: "2024-05-29T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *International Conference on Machine Learning (ICML)*
publication_short: In *International Conference on Machine Learning (ICML)*

abstract: The study of behavioral diversity in Multi-Agent Reinforcement Learning (MARL) is a nascent yet promising field. In this context, the present work deals with the question of how to control the diversity of a multi-agent system. With no existing approaches to control diversity to a set value, current solutions focus on blindly promoting it via intrinsic rewards or additional loss functions, effectively changing the learning objective and lacking a principled measure for it. To address this, we introduce Diversity Control (DiCo), a method able to control diversity to an exact value of a given metric by representing policies as the sum of a parameter-shared component and dynamically scaled per-agent components. By applying constraints directly to the policy architecture, DiCo leaves the learning objective unchanged, enabling its applicability to any actor-critic MARL algorithm. We theoretically prove that DiCo achieves the desired diversity, and we provide several experiments, both in cooperative and competitive tasks, that show how DiCo can be employed as a novel paradigm to increase performance and sample efficiency in MARL. Multimedia results are available on the [paper's website](https://sites.google.com/view/dico-marl).
summary: We introduce Diversity Control (DiCo), a method able to control diversity to an exact value of a given metric by representing policies as the sum of a parameter-shared component and dynamically scaled per-agent components. By applying constraints directly to the policy architecture, DiCo leaves the learning objective unchanged, enabling its applicability to any actor-critic MARL algorithm. We theoretically prove that DiCo achieves the desired diversity, and we provide several experiments, both in cooperative and competitive tasks, that show how DiCo can be employed as a novel paradigm to increase performance and sample efficiency in MARL.
  
tags:
- Multi-Agent Reinforcement Learning
- Heterogeneity

featured: true

links:
- name: Website
  url: https://sites.google.com/view/dico-marl
- name: OpenReview
  url: https://openreview.net/forum?id=qQjUgItPq4
- name: arXiv
  url: https://arxiv.org/abs/2405.15054
- name: Poster
  url: poster.pdf
- name: Talk
  url: https://youtu.be/ImcuXnmX43g
url_pdf: ''
url_code: 'https://github.com/proroklab/ControllingBehavioralDiversity'
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
  placement: 3
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