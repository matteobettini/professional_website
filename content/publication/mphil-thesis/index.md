---
title: "Transport network design for vehicle routing: results on path addition and capacity reduction"
authors:
- admin

date: "2021-06-04T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["7"]

# Publication name and optional abbreviated publication name.
publication: MPhil Thesis
publication_short: MPhil Thesis

abstract: Autonomous Vehicles (AVs) are becoming increasingly popular thanks to advancements in Artificial Intelligence algorithms that enable self-driving. This technological shift will lead to a drastic change in our current mobility paradigms. Historic trends suggest that this change will heavily impact the transportation infrastructure. While a lot of works focus on control and routing of AVs, little attention is being paid to the transportation network. In this thesis, we investigate the problem of optimising the transportation network for AVs both from a theoretical and from a practical perspective. In the first part, we investigate the properties of adding paths to a network and prove that the intuitive statement "adding a path to a transport network always grants greater or equal benefit to users than adding it to a bigger network" is false. In other words, we prove that path additions to transport networks, where AVs are routed, are not supermodular in travel time, extending the seminal result of Braess' paradox. We provide counterexamples to support our proofs. We further provide some formulations where, instead, we are able to prove the supermodularity of path additions. In the second part, we formulate two network design problems for self-interested AVs. We present the problem of optimising transport networks via path additions and a novel problem design where self-interested users are guided towards optimal paths through the reduction of road capacities. This formulation, unlike previous network design research, allows users to see non-optimal roads as more costly by bridging a road pricing policy with environment shaping. To solve the capacity reduction problem, we implement a genetic algorithm as well as a reinforcement learning task using a designer agent trained with proximal policy optimisation and a graph neural network architecture. We simulate our solutions in the microscopic traffic simulator SUMO and in a custom built macroscopic traffic simulator. Through capacity reductions, we achieve significant total travel time improvements on six real-world transport networks&#58; Anaheim (USA), Barcelona (Spain), Chicago (USA), Eastern Massachusetts (USA), Sioux Falls (USA), and Winnipeg (Canada). For instance, we improve the Chicago network by up to 7%, saving more than 487 hours of total travel time per traffic hour. This is done strictly through virtual capacity reductions, without the need for physical or infrastructural modifications to the network. This makes our solutions ready for immediate deployment on any transport network in the world.
summary: In this thesis, we investigate the problem of optimising the transportation network for AVs both from a theoretical and from a practical perspective. In the first part, we investigate the properties of adding paths to a network and we prove that path additions to transport networks, where AVs are routed, are not supermodular in travel time, extending the seminal result of Braess’ paradox.  In the second part, we formulate two network design problems for self-interested AVs. We present the problem of optimising transport networks via path additions and a novel problem design where self-interested users are guided towards optimal paths through the reduction of road capacities.  Through capacity reductions, we achieve significant total travel time improvements on six real-world transport networks&#58; Anaheim (USA), Barcelona (Spain), Chicago (USA), Eastern Massachusetts (USA), Sioux Falls (USA), and Winnipeg (Canada). For instance, we improve the Chicago network by up to 7%, saving more than 487 hours of total travel time per traffic hour. 

tags:


featured: false

url_pdf: ''
url_code: 'https://github.com/matteobettini/Traffic-Assignment-Frank-Wolfe-2021'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://youtu.be/FPbyjnwUizQ'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Traffic improvements.'
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