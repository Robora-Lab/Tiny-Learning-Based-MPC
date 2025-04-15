---
layout: post
title: "UAV-USV Landing"
author: Jess Stephenson, Melissa Greeff, William S. Stewart, Nathan T. Duncan
---

Welcome to the UAV-USV Landing project. This page covers the progress made on this project to date.

## Background
Autonomous teams of multirotors and uncrewed surface vessels (USVs) are invaluable to challenging maritime applications, including remote monitoring, search-and-rescue, and surveillance [1], [2], [3]. After deployment in a remote setting, the functional life of the system is ultimately limited by the battery-life of the multirotor. The research that I continue to investigate is the ability to autonomously land a multirotor on a USV for recharging. We address this problem with safe control algorithms and apply control schemes in simulation, testbed validation, and real-world experiments.

Operating in unknown and variable marine conditions, USVs are subject to complex wave-induced motions that include effects on pitch, roll, yaw, sway, surge, and heave [4]. To prevent damage to the multirotor due to severe motion in these degrees of freedom, it must perform a safe and controlled landing [5]. In a robust landing solution, we must consider the variability of the amplitude and frequency of waves due to changing meteorological conditions. We leverage the Great Lakes Coastal Forecasting System to define the range of waves in which our system should succeed.

## Stage 3: 
###### Winter 2025
###### Accepted to the workshop '25 Years of Aerial Robotics: Challenges and Opportunities' hosted at the 2025 International Conference on Robotics and Automation (ICRA)

While the aforementioned work considers harsh waves and resolves two key limitations of the initial solution, we still assume that there is a local region with calm waves that can be reached by both vehicles to then perform a safe landing. In practical scenarios, spatial-temporal assumptions are not realistic if an emergency landing is necessary or if time and resources are constrained. Recognizing that robust multirotor landing on a USV requires safe landing in waves of varying severity, we benchmark the robustness of three different quadratic MPC strategies for landing on the tilting testbed under various frequency and amplitude conditions. In these strategies we include optimization costs that weigh position, attitude, and altitude errors between the multirotor and the platform. Though all strategies successfully land in low-frequency, low-amplitude conditions, they have low success in the higher-amplitude conditions. In this work, we conclude that quadratic MPC cost is not robust to the range of frequencies and amplitudes required for landing in waves.

## References
[1]	Y. Wang, W. Liu, J. Liu, and C. Sun, “Cooperative USV–UAV marine search and rescue with visual navigation and reinforcement learning-based control,” ISA Trans., vol. 137, pp. 222–235, 2023.
[2]	J. Wu, R. Li, J. Li, M. Zou, and Z. Huang, “Cooperative unmanned surface vehicles and unmanned aerial vehicles platform as a tool for coastal monitoring activities,” Ocean Coast. Manag., vol. 232, p. 106421, 2023
[3]	A. Vasilijevic et al., “Heterogeneous robotic system for underwater oil spill survey,” in OCEANS 2015 - Genova, pp. 1–7, 2015.
[4]	T. I. Fossen, Handbook of marine craft hydrodynamics and motion control. John Wiley & Sons, 2011.
[5]	K. Xia, M. Shin, W. Chung, M. Kim, S. Lee, and H. Son, “Landing a quadrotor UAV on a moving platform with sway motion using robust control,” Control Eng. Pract., vol. 128, p. 105288, 2022.
