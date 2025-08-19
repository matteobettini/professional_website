---
title: "Neural diversity in multi-agent learning"
authors:
- admin

date: "2025-08-19T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["7"]

# Publication name and optional abbreviated publication name.
publication: PhD Thesis
publication_short: PhD Thesis

abstract: Collective intelligence is key to life and pervasive in natural systems. Despite its importance, this emergent property remains largely unknown to us. While studies in natural systems have identified diversity as one of the core principles leading to its emergence, research in collective artificial intelligence has left diversity largely underexplored.<br><br>The lack of work studying behavioural diversity in multi-agent learning is due to traditional approaches constraining the agents' strategies to be identical. This speeds up learning by training a shared policy from all individuals' experiences, but results in the agents becoming behaviourally homogeneous. Homogeneous agents are forced to take the same action given the same input, thus losing diversity in their strategies. This issue is more evident in the context of multi-agent reinforcement learning (MARL), where homogeneous training is used to ameliorate the high computational costs of simulation. While there are works focused on boosting behavioural diversity in MARL, they just promote it via additional losses or intrinsic rewards, without a principled method to measure or control it. In doing so, they effectively change the learning objective of the original task, compromising its optimality.<br><br>The aim of this thesis is to crystallise the role of neural (i.e. behavioural) diversity in collective artificial intelligence by studying its impact on multi-agent learning. Towards this goal, we introduce HetGPPO&#58; a novel graph neural network (GNN) model that allows agents to learn and communicate heterogeneously. We deploy HetGPPO on a fleet of ground robots, demonstrating the intrinsic noise-resilience provided by neural diversity in real-world multi-robot tasks. To quantify the resulting heterogeneity, we present system neural diversity (SND), a novel metric of behavioural heterogeneity in multi-agent learning. SND is the first metric to allow diversity comparison across systems of different sizes and quantification of behavioural redundancy. Finally, we employ SND in diversity control (DiCo), the first method able to control the diversity of a multi-agent system to an exact value of a given metric. DiCo is the only method able to constrain diversity without the addition of learning objectives, doing so via structural constraints to the agents’ policy networks. We employ SND and DiCo in a large-scale empirical study on the impact of diversity in cooperative and competitive tasks. In multi-agent simulated soccer, with up to five players per team, our results show that controlling diversity leads to the emergence of novel strategies such as passing and goal-keeping, outperforming homogeneous agents and demonstrating the need for behavioural roles.<br><br>To support the study of neural diversity, we introduce several novel open-source libraries for simulating and training multi-agent systems (MAS). Firstly, we present the vectorised multi-agent simulator (VMAS), a batched simulator containing a collection of multi-robot tasks written in PyTorch. Thanks to graphics processing unit (GPU) acceleration and batching, VMAS offers incredible speed-ups with respect to previous state-of-the-art software. Secondly, we introduce BenchMARL, a MARL training library with the goal of standardising benchmarking and enabling reproducibility in multi-agent reinforcement learning. BenchMARL provides high-performance and maintained state-of-the-art implementations that allow comparisons across different algorithms, models, and environments.<br><br>This thesis presents a study of neural diversity in MAS, demonstrating its key, though previously ignored, role in collective learning. We introduce novel methods to simulate, enable, train, measure, and control neural diversity in multi-agent learning. The results gathered show that neural diversity is fundamental for cooperation, exploration, and resilience, paving the way towards the understanding and development of collective artificial general intelligence.

summary: This thesis presents a study of neural diversity in multi-agent systems, demonstrating its key, though previously ignored, role in collective learning. We introduce novel methods to simulate, enable, train, measure, and control neural diversity in multi-agent reinforcement learning. The results gathered show that neural diversity is fundamental for cooperation, exploration, and resilience, paving the way towards the understanding and development of collective artificial general intelligence.

tags:
- Multi-Agent Reinforcement Learning
- Heterogeneity

featured: false

links:
- name: University of Cambridge
  url: https://www.repository.cam.ac.uk/handle/1810/388334
url_pdf: 'https://www.repository.cam.ac.uk/handle/1810/388334'
url_code: ''
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