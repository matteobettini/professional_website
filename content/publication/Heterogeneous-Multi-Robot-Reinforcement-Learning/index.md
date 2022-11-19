---
title: "Heterogeneous Multi-Robot Reinforcement Learning"
authors:
- admin
- shankar
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
publication: In *Proc. of the 22nd International Conference on Autonomous Agents and Multiagent Systems (AAMAS)*
publication_short: In *Proc. of the 22nd International Conference on Autonomous Agents and Multiagent Systems (AAMAS)*

abstract: Cooperative multi-robot tasks can benefit from heterogeneity in the robots’ physical and behavioral traits. In spite of this, traditional Multi-Agent Reinforcement Learning (MARL) frameworks lack the ability to explicitly accommodate policy heterogeneity, and typically constrain agents to share neural network parameters. This enforced homogeneity limits application in cases where the tasks benefit from heterogeneous behaviors. In this paper, we crystallize the role of heterogeneity in MARL policies. Towards this end, we introduce Heterogeneous Graph Neural Network Proximal Policy Optimization (HetGPPO), a paradigm for training heterogeneous MARL policies that leverages a Graph Neural Network for differentiable inter-agent communication. HetGPPO allows communicating agents to learn heterogeneous behaviors while enabling fully decentralized training in partially observable environments. We complement this with a taxonomical overview that exposes more heterogeneity classes than previously identified. To motivate the need for our model, we present a characterization of techniques that homogeneous models can leverage to emulate heterogeneous behavior, and show how this “apparent heterogeneity” is brittle in real-world conditions. Through simulations and real-world experiments, we show that&#58; (i) when homogeneous methods fail due to strong heterogeneous requirements, HetGPPO succeeds, and, (ii) when homogeneous methods are able to learn apparently heterogeneous behaviors, HetGPPO achieves higher resilience to both training and deployment noise.

# Summary. An optional shortened abstract.
summary:  In this paper, we crystallize the role of heterogeneity in MARL policies.We introduce Heterogeneous Graph Neural Network Proximal Policy Optimization (HetGPPO), a paradigm for training heterogeneous MARL policies that leverages a Graph Neural Network for differentiable inter-agent communication. HetGPPO allows communicating agents to learn heterogeneous behaviors while enabling fully decentralized training in partially observable environments. Through simulations and real-world experiments, we show that&#58; (i) when homogeneous methods fail due to strong heterogeneous requirements, HetGPPO succeeds, and, (ii) when homogeneous methods are able to learn apparently heterogeneous behaviors, HetGPPO achieves higher resilience to both training and deployment noise.

tags:
- Heterogeneity
- Multi-Agent Reinforcement Learning
categories: 
- Heterogeneity
- Multi-Agent Reinforcement Learning
featured: true

links:
- name: arXiv
  url: 
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