---
title: " Sampling-Based Motion Planning with Dynamics Focused on Computational Efficiency"
excerpt: "a re-implementation of the GUided Sampling
          Tree (GUST) algorithm, originally developed by [Plaku(2015)]"
collection: portfolio
---

Planning algorithms for robotics are typically designed and tested in simulated environments, often involving a point robot navigating a flat terrain. However, these simulations fail to capture the complexities and challenges posed by real world scenarios, such as a car driving on rough terrain. In such scenarios, it becomes crucial to account for both the kinematics and dynamics of the car in the planning process, resulting in the need for high-dimensional planning. Yet, high-dimensional planning problems can be computationally complex, necessitating the use of efficient planning algorithms. Therefore, we present a re-implementation of the GUided Sampling Tree (GUST) algorithm, originally developed by [Plaku(2015)], to effectively addresses this challenge. This algorithm's key insights include the partitioning of the workspace and motion tree into sub-regions, enabling efficient and swift path generation, as well as computing heuristics for the workspace only once. Our re-implementation of GUST yielded an approximately 3 times faster planning time than the Rapidly-Exploring Random Tree (RRT) algorithm in both goal-biased an non-goal-biased settings for our most complex map. We visualized this in simulation environments.
![GUST](/images/portfolio/GUST.gif)
