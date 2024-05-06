---
title: "The Cambridge RoboMaster: An Agile Multi-Robot Research Platform"
authors:
- blumenkamp
- shankar
- admin
- Joshua Bird
- prorok


date: "2024-05-05T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: In *Preprint*
publication_short: In *Preprint*

abstract: Compact robotic platforms with powerful compute and actuation capabilities are key enablers for practical, real-world deployments of multi-agent research. This article introduces a tightly integrated hardware, control, and simulation software stack on a fleet of holonomic ground robot platforms designed with this motivation. Our robots, a fleet of customised DJI Robomaster S1 vehicles, offer a balance between small robots that do not possess sufficient compute or actuation capabilities and larger robots that are unsuitable for indoor multi-robot tests. They run a modular ROS2-based optimal estimation and control stack for full onboard autonomy, contain ad-hoc peer-to-peer communication infrastructure, and can zero-shot run multi-agent reinforcement learning (MARL) policies trained in our vectorized multi-agent simulation framework. We present an in-depth review of other platforms currently available, showcase new experimental validation of our system's capabilities, and introduce case studies that highlight the versatility and reliabilty of our system as a testbed for a wide range of research demonstrations. Our system as well as supplementary material is available online at [this https URL](https://proroklab.github.io/cambridge-robomaster/).
# Summary. An optional shortened abstract.
summary: This article introduces a tightly integrated hardware, control, and simulation software stack on a fleet of holonomic ground robot platforms. Our robots, a fleet of customised DJI Robomaster S1 vehicles, offer a balance between small robots that do not possess sufficient compute or actuation capabilities and larger robots that are unsuitable for indoor multi-robot tests.
  
tags:
- Multi-Agent Reinforcement Learning

featured: false

links:
- name: Docs
  url: https://proroklab.github.io/cambridge-robomaster/
- name: arXiv
  url: https://arxiv.org/abs/2405.02198
url_pdf: ''
url_code: 'https://github.com/proroklab/cambridge-robomaster'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://proroklab.github.io/cambridge-robomaster/supplementary.html#vmas-deployment'

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