---
title: "An optimization-based planner with b-spline parameterized continuous-time reference signals"
authors:
  - Chuyuan Tao
  - Sheng Cheng
  - Fanxin Wang
  - Yang Zhao
  - Naira Hovakimyan
date: "2024-10-14"

# Schedule page publish date (NOT publication's date).
publishDate: "2024-10-14"

# Publication name and optional abbreviated publication name.
publication: "2024 IEEE/RSJ International Conference on Intelligent Robots and Systems"
publication_short: "IROS"

abstract: For the cascaded planning and control modules implemented for robot navigation, the frequency gap between the planner and controller has received limited attention. In this study, we introduce a novel B-spline parameterized optimization-based planner (BSPOP) designed to address the frequency gap challenge with limited onboard computational power in robots. The proposed planner generates continuous-time control inputs for low-level controllers running at arbitrary frequencies to track. Furthermore, when considering the convex control action sets, BSPOP uses the convex hull property to automatically constrain the continuous-time control inputs within the convex set. Consequently, compared with the discrete-time optimization-based planners, BSPOP reduces the number of decision variables and inequality constraints, which improves computational efficiency as a byproduct. Simulation results demonstrate that our approach can achieve a comparable planning performance to the high-frequency baseline optimization-based planners while demanding less computational power. Both simulation and experiment results show that the proposed method performs better in planning compared with baseline planners in the same frequency.

# Summary. An optional shortened abstract.
summary: 

tags:
- Motion Planning
- Optimization
- Model Predictive Control
featured: true

links:
  - type: pdf
    url: https://ieeexplore.ieee.org/abstract/document/11311503
  - type: video
    url: https://www.youtube.com/watch?v=mQK9Md8BxRA

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: true

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
