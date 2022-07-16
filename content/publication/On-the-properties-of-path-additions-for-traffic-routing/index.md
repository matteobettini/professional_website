---
title: "On the Properties of Path Additions for Traffic Routing"
authors:
- admin
- prorok
date: "2022-02-06T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication:
publication_short: In *Preprint* 

abstract: In this paper we investigate the impact of path additions to transport networks with optimised traffic routing. In particular, we study the behaviour of total travel time, and consider both self-interested routing paradigms, such as User Equilibrium (UE) routing, as well as cooperative paradigms, such as classic Multi-Commodity (MC) network flow and System Optimal (SO) routing. We provide a formal framework for designing transport networks through iterative path additions, introducing the concepts of trip spanning tree and trip path graph. Using this formalisation, we prove multiple properties of the objective function for transport network design. Since the underlying routing problem is NP-Hard, we investigate properties that provide guarantees in approximate algorithm design. Firstly, while Braess' paradox has shown that total travel time is not monotonic non-increasing with respect to path additions under self-interested routing (UE), we prove that, instead, monotonicity holds for cooperative routing (MC and SO). This result has the important implication that cooperative agents make the best use of redundant infrastructure. Secondly, we prove via a counterexample that the intuitive statement "adding a path to a transport network always grants greater or equal benefit to users than adding it to a superset of that network" is false. In other words, we prove that, for all the routing formulations studied, total travel time is not supermodular with respect to path additions. While this counter-intuitive result yields a hardness property for algorithm design, we provide particular instances where, instead, the property of supermodularity holds.  Our study on monotonicity and supermodularity of total travel time with respect to path additions provides formal proofs and scenarios that constitute important insights for transport network designers.

# Summary. An optional shortened abstract.
summary: In this paper, we investigate the impact of path additions to transport networks with optimised traffic routing. In particular, we study the behaviour of total travel time, and consider both self-interested routing paradigms, such as User Equilibrium (UE) routing, as well as cooperative paradigms, such as classic Multi-Commodity (MC) network flow and System Optimal (SO) routing. This work aims to provide an analysis and categorization of the properties of objective functions for transport network design, with the purpose of informing algorithm (and also network) designers. Among our results, we prove, via counterexample, that total travel time, under both cooperative and self-interested routing, is not supermodular with respect to path additions. 


tags:
- Transport Network Design
featured: false

links:
- name: arXiv
  url: https://arxiv.org/abs/2207.04505
url_pdf:
url_code: 'https://github.com/matteobettini/Traffic-Assignment-Frank-Wolfe-2021'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Non-supermodularity of path additions'
  focal_point: "Center"
  preview_only: false
  placement: 1

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
