---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

I am broadly interested in machine learning, control, and optimization. My long-term goal is to make AI-enabled autonomous systems work safely and reliably in the real world. 

## Scalable Neural Network Verification
<img src="/files/admm_module.png" alt="ADMM modules for NN verification" width="100"/>
<!-- <img src="/files/admm_module.png" width="100"/> -->

Neural network verification considers the problem of certifying if the output of a NN satisfies certain properties for a given input set. This is a fundamental problem in certifying the robustness of NNs and the safety of NN-controlled systems. 

In [J2](https://ieeexplore.ieee.org/abstract/document/9811356), we use Alternating Direction Method of Multipliers (ADMM) to derive a NN verification method, DeepSplit, that is scalable, modular, amenable to GPU acceleration and enjoys fast theoretical convergence guarantees. 

## Safety and stability analysis of learning-enabled systems
<img src="/files/ROA_NN.png" alt="region of attraction estimation of NN-controlled system" width="200"/>

Learning for control works great, but the gap between research in labs and deployment in the real world is hard to close. The coupling of learning modules and dynamical systems significantly complicates the analysis of the system's behavior. How can we make this leap to achieve assured autonomy?

For learning-enabled systems, we analyze their reachability in [C9](https://arxiv.org/abs/2209.11827) and stability in [C6](https://arxiv.org/abs/2012.12015), [C7](https://arxiv.org/abs/2110.00731). In reachability analysis, we rigorously characterize the conservatism-complexity trade-off when using NN verification tools. In stability analysis, we draw tools from convex optimization to learn a Lyapunov function with convergence guarantees.

## Boosting tightness of robust model predictive control
<img src="/files/random_comparison.png" alt="Tightness comparison of robust MPC methods on random examples. The higher the better." width="50"/>

Model predictive control (MPC) is widely applied in robotic and cyber-physical systems. Robust MPC takes model uncertainties and disturbances explicitly into account when designing feedback policies. It gives rise to a challenging robust optimization problem where the effects of uncertainty and feedback policy are intertwined. 

In [J4](https://arxiv.org/pdf/2203.11375.pdf),  we propose a novel robust MPC method, SLS MPC, using System Level Synthesis and search for robust feedback controllers in the space of closed-loop system responses. This parameterization reveals additional structured properties of the robust control problem and leads to a significant tightness improvement of robust MPC. 

## Online safety filter design for learning-enabled systems
<img src="/files/gauge_CBF.png" alt="Safe-by-construction NN controller using a control barrier function." width="200"/>

A safety filter monitors the output of a reference policy online and corrects any unsafe actions to guarantee the safety of the system. It enjoys modularity and theoretical soundness, making it a popular and promising tool for safe learning-based control. However, it remains a challenge to design a safety filter for complex dynamics. 

In [C10](https://arxiv.org/abs/2308.08086), we design a convex optimization-based predictive safety filter for NN dynamical systems by fusing NN verification with robust MPC.  In [J3](https://arxiv.org/abs/2209.10034), we propose a safe-by-construction NN policy using control barrier functions. 
