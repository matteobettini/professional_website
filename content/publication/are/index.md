---
title: "ARE: Scaling Up Agent Environments and Evaluations"
authors:
- Pierre Andrews
- Amine Benhalloum
- Gerard Moreno-Torres Bertran
- admin
- Amar Budhiraja
- Ricardo Silveira Cabral
- Virginie Do
- Romain Froger
- Emilien Garreau
- Jean-Baptiste Gaya
- Hugo Laurençon
- Maxime Lecanu
- Kunal Malkan
- Dheeraj Mekala
- Pierre Ménard
- Grégoire Mialon
- Ulyana Piterbarg
- Mikhail Plekhanov
- Mathieu Rita
- Andrey Rusakov
- Thomas Scialom
- Vladislav Vorotilov
- Mengjue Wang
- Ian Yu
date: "2026-04-20T00:00:00Z"
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


abstract: We introduce Meta Agents Research Environments (ARE), a research platform for scalable creation of environments, integration of synthetic or real applications, and execution of agentic orchestrations. ARE provides simple abstractions to build complex and diverse environments, each with their own rules, tools, content, and verifiers, helping to bridge the gap between model development and real-world deployment. We also propose Gaia2, a benchmark built in ARE and designed to measure general agent capabilities. Beyond search and execution, Gaia2 requires agents to handle ambiguities and noise, adapt to dynamic environments, collaborate with other agents, and operate under temporal constraints. Unlike prior benchmarks, Gaia2 runs asynchronously, surfacing new failure modes that are invisible in static settings. Our experiments show that no system dominates across the intelligence spectrum&#58; stronger reasoning often comes at the cost of efficiency, and budget scaling curves plateau, highlighting the need for new architectures and adaptive compute strategies. Perhaps more importantly, ARE abstractions enable continuous extension of Gaia2 to other environments, empowering the community to rapidly create new benchmarks tailored to their domains. In AI's second half, progress increasingly depends on defining meaningful tasks and robust evaluations to drive frontier capabilities forward.# Summary. An optional shortened abstract.
summary: We introduce Meta Agents Research Environments (ARE), a research platform for scalable creation of environments, integration of synthetic or real applications, and execution of agentic orchestrations. We also propose Gaia2, a benchmark built in ARE and designed to measure general agent capabilities. Unlike prior benchmarks, Gaia2 runs asynchronously, surfacing new failure modes that are invisible in static settings.

tags:
- Software library
- LLM Agents
featured: True

links:
- name: Docs
  url: https://facebookresearch.github.io/meta-agents-research-environments/
- name: arXiv
  url: https://arxiv.org/abs/2509.17158v1
- name: Demo
  url: https://huggingface.co/spaces/meta-agents-research-environments/demo
- name: Meta AI
  url: https://ai.meta.com/research/publications/are-scaling-up-agent-environments-and-evaluations/
- name: Leaderboard
  url: https://huggingface.co/spaces/meta-agents-research-environments/leaderboard
- name: Post
  url: https://huggingface.co/blog/gaia2
- name: OpenReview
  url: https://openreview.net/forum?id=9gw03JpKK4
url_pdf:
url_code: 'https://github.com/facebookresearch/meta-agents-research-environments'
url_dataset: 'https://huggingface.co/datasets/meta-agents-research-environments/gaia2'
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