---
title: "System Neural Diversity: Measuring Behavioral Heterogeneity in Multi-Agent Learning"
authors:
- admin
- shankar
- prorok
date: "2023-04-01T00:00:00Z"
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

abstract: Evolutionary science provides evidence that diversity confers resilience in natural systems. Yet, traditional multi-agent reinforcement learning techniques commonly enforce homogeneity to increase training sample efficiency. When a system of learning agents is not constrained to homogeneous policies, individuals may develop diverse behaviors, resulting in emergent complementarity that benefits the system. Despite this, there is a surprising lack of tools that quantify behavioral diversity. Such techniques would pave the way towards understanding the impact of diversity in collective artificial intelligence and enabling its control. In this paper, we introduce System Neural Diversity (SND)&#58; a measure of behavioral heterogeneity in multi-agent systems. We discuss and prove its theoretical properties, and compare it with alternate, state-of-the-art behavioral diversity metrics used in the robotics domain. Through simulations of a variety of cooperative multi-robot tasks, we show how our metric constitutes an important tool that enables measurement and control of behavioral heterogeneity. In dynamic tasks, where the problem is affected by repeated disturbances during training, we show that SND allows us to measure latent resilience skills acquired by the agents, while other proxies, such as task performance (reward), fail to. Finally, we show how the metric can be employed to control diversity, allowing us to enforce a desired heterogeneity set-point or range. We demonstrate how this paradigm can be used to bootstrap the exploration phase, finding optimal policies faster, thus enabling novel and more efficient MARL paradigms.
# Summary. An optional shortened abstract.
summary: In this paper, we introduce System Neural Diversity (SND)&#58; a measure of behavioral heterogeneity for multi-agent systems where agents have stochastic policies. We discuss and prove its theoretical properties, and compare it with alternate, state-of-the-art behavioral diversity metrics used in cross-disciplinary domains. Through simulations of a variety of multi-agent tasks, we show how our metric constitutes an important diagnostic tool to analyze latent properties of behavioral heterogeneity.

tags:
- Heterogeneity
- Multi-Agent Reinforcement Learning
featured: False

links:
- name: arXiv
  url: https://arxiv.org/abs/2305.02128
url_pdf:
url_code: 'https://github.com/proroklab/HetGPPO'
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