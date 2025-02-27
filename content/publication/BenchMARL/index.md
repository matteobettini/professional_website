---
title: "BenchMARL: Benchmarking Multi-Agent Reinforcement Learning"
authors:
- admin
- prorok
- Vincent Moens

date: "2024-05-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *Journal of Machine Learning Research (JMLR)*
publication_short: In *Journal of Machine Learning Research (JMLR)*

abstract: The field of Multi-Agent Reinforcement Learning (MARL) is currently facing a reproducibility crisis. While solutions for standardized reporting have been proposed to address the issue, we still lack a benchmarking tool that enables standardization and reproducibility, while leveraging cutting-edge Reinforcement Learning (RL) implementations. In this paper, we introduce BenchMARL, the first MARL training library created to enable standardized benchmarking across different algorithms, models, and environments. BenchMARL uses TorchRL as its backend, granting it high performance and maintained state-of-the-art implementations while addressing the broad community of MARL PyTorch users. Its design enables systematic configuration and reporting, thus allowing users to create and run complex benchmarks from simple one-line inputs.
# Summary. An optional shortened abstract.
summary: BenchMARL is a library for benchmarking Multi-Agent Reinforcement Learning (MARL) using TorchRL. BenchMARL allows to quickly compare different MARL algorithms, tasks, and models while being systematically grounded in its two core tenets&#58; reproducibility and standardization.

tags:
- Multi-Agent Reinforcement Learning
- Software library

featured: true

links:
- name: Docs
  url: https://benchmarl.readthedocs.io/
- name: Wandb Benchmarks
  url: https://wandb.ai/matteobettini/benchmarl-public/reportlist
- name: Talk
  url: https://www.youtube.com/watch?v=1tOIMgJf_VQ
- name: Lecture
  url: https://www.youtube.com/watch?v=mIb1uGeRJsg
- name: arXiv
  url: https://arxiv.org/abs/2312.01472
- name: Poster
  url: poster.pdf
- name: Proceedings
  url: http://jmlr.org/papers/v25/23-1612.html
- name: NeurIPS
  url: https://neurips.cc/virtual/2024/poster/98318
url_pdf: ''
url_code: 'https://github.com/facebookresearch/BenchMARL'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'BenchMARL execution diagram'
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