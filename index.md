---
layout: post
title: "Tiny Learning-Based MPC for Multirotors"
author: Babak Akbari, Justin Frank, Melissa Greeff
---


We present a **computationaly efficient learning-based algorithm** for **tiny multirotors** under aerodynamic disturbances.

This project is based on two recent papers:

- **Tiny Learning-Based MPC for Multirotors: Solver-Aware Learning for Efficient Embedded Predictive Control**  
  [arXiv link](https://arxiv.org/abs/2410.23634)

- **A Computationally Efficient Learning-Based MPC for Multirotors Under Aerodynamic Disturbances**  
  [IEEE link](https://ieeexplore.ieee.org/document/10557089)

---

### 🧭 Motivation

Tiny UAVs must navigate cluttered environments and handle aerodynamic drag, propwash, and wind — all on minimal compute. Our work targets:

- **Embedded efficiency**: Optimizing for onboard solvers with low runtime and memory overhead
- **Disturbance robustness**: Learning dynamics-aware policies resilient to aerodynamic effects

---

### ⚙️ Approach Summary

#### Learning-Based Dynamics Modeling

We construct **data-driven models** that capture multirotor dynamics and external disturbances (like drag) via supervised learning from flight data.

#### Solver-Aware MPC

We use **differentiable programming** and **trajectory optimization-aware training** to learn dynamics models that are easy to optimize within MPC.

#### Real-Time Implementation

Our policies are deployed onboard resource-limited platforms using optimized CVXPY-based solvers and minimal memory.

---

### ✈️ Key Results

- **<10 ms solve time** for MPC problems onboard a Teensy 4.0
- Robust flight in presence of **significant drag**
- Trajectory tracking in cluttered environments
- Learning methods that are compatible with **real-time solvers**

---

### 📸 Visual Examples

#### Flight with and without learned disturbance model

| No Compensation | With Learned Drag Model |
|-----------------|--------------------------|
| ![No Drag](images/no_drag.png) | ![With Drag](images/with_drag.png) |

---

### 📹 Demonstration Video

<div align="center">
  <video width="640" height="360" controls>
    <source src="flight_demo.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

---

### 📄 Citation

If you use this work, please cite:

```bibtex
@article{rao2024tiny,
  title={Tiny Learning-Based MPC for Multirotors: Solver-Aware Learning for Efficient Embedded Predictive Control},
  author={Rao, Apurva and Zhang, Yuheng and Tsiamis, Alexandros and Alonso-Mora, Javier and Kolter, Zico and Schmerling, Edward},
  journal={arXiv preprint arXiv:2410.23634},
  year={2024}
}

@inproceedings{rao2024computationally,
  title={A Computationally Efficient Learning-Based Model Predictive Control for Multirotors Under Aerodynamic Disturbances},
  author={Rao, Apurva and Zhang, Yuheng and Schmerling, Edward},
  booktitle={2024 IEEE International Conference on Robotics and Automation (ICRA)},
  year={2024},
  organization={IEEE}
}
