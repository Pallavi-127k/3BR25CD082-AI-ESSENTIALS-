# 🚦 Smart Traffic Lights Using Local AI

[![IEEE Standard](https://img.shields.io/badge/Format-IEEE%20Conference-blue)](https://www.ieee.org/)
[![Topic](https://img.shields.io/badge/Focus-Edge%20AI%20%26%20Traffic%20Control-green)](#)

---

## 📌 Executive Summary & Project Overview

Urban traffic congestion remains a critical challenge for modern cities. Traditional traffic signals rely on static, fixed-time schedules that fail to adapt to sudden changes in vehicular density or emergency situations.

This repository presents research and implementation details on **Smart Traffic Lights Using Local AI (Edge AI)**, based on the **AI-Assisted Research & LaTeX Workshop** ("AI Essentials") coursework. The project investigates adaptive traffic signal control systems, comparing traditional fixed timers, centralized cloud-based AI, and decentralized local edge processing. Additionally, it highlights key research gaps in real-time emergency vehicle routing and traffic path coordination.

---

## 🏗️ System Architecture

The proposed smart traffic system operates on a decentralized, multi-tiered edge computing architecture divided into four core steps:

```
[ Street Cameras ] ──► [ Smart Pole Computers (Edge) ] ──► [ Traffic Lights ]
                                  │
                                  ▼
                        [ City Cloud Server ]
```

1. **📷 Street Cameras**: Continuous video feeds capture real-time road conditions at intersections.
2. **💻 Smart Pole Computers (Local Edge AI)**: Local processing units analyze live video streams, estimate vehicle density using computer vision/machine learning models, and execute rapid traffic control decisions locally.
3. **☁️ City Cloud Server**: Summary statistics and long-term analytical data are forwarded to the central city server for macro-level storage, monitoring, and historical traffic planning.
4. **🚦 Traffic Lights**: Intersection controllers receive immediate instructions from local edge nodes to dynamically adapt signal phase timings.

---

## 📊 System Comparison Matrix

A comparative evaluation of traffic control paradigms highlights the trade-offs between decision latency, bandwidth consumption, and infrastructure costs:

| System Architecture | Decision Latency | Data Bandwidth Usage | Initial Setup Cost | Key Characteristics |
| :--- | :---: | :---: | :---: | :--- |
| **Basic Timed Lights** | `30.0 s` | **Zero** | **$200** | Static timing; incapable of responding to traffic bursts. |
| **Cloud AI Systems** | `2.0 s` | **High** | **$2,500** | High compute power, but dependent on persistent internet & higher latency. |
| **Local Smart Cameras (Edge AI)** | `0.5 s` | **Low** | **$1,200** | Ultra-low latency decision making, resilient offline operation, minimized data transfer. |

---

## 📚 Literature Review & Citation Evaluation

The research builds upon existing studies in machine vision and reinforcement learning for traffic signal control:

1. **Deep Reinforcement Learning**:
   * *F. Rasheed, K.-L. A. Yau, R. M. Noor, C. Wu, and Y.-C. Low*, **"Deep reinforcement learning for traffic signal control: A review"**, *IEEE Access*, vol. 8, pp. 208016–208044, 2020.
   * *Insight*: Analyzes DRL algorithms for optimizing signal light phases based on dynamic multi-intersection feedback.

2. **Machine Vision & Adaptive Timing**:
   * *V. Gorodokin, S. Zhankaziev, E. Shepeleva, K. Magdin, and S. Evtyukov*, **"Optimization of adaptive traffic light control modes based on machine vision"**, *Transportation Research Procedia*, vol. 57, pp. 241–249, 2021.
   * *Insight*: Demonstrates adaptive timing adjustments using vision-based vehicle detection to alleviate local intersection queues.

---

## 🔍 Research Gap & Future Directions

* **Emergency Vehicle Prioritization**: Current adaptive systems function effectively under standard traffic flow conditions, but often lack automated, multi-intersection coordination for emergency vehicles (e.g., ambulances, fire engines).
* **Proposed Extension**: Developing edge-to-edge communication protocols allowing approaching emergency vehicles to broadcast signal preemptions, dynamically clearing green corridors across consecutive intersections in real time.

---

## 📂 Repository Contents

| File Name | Description |
| :--- | :--- |
| `3BR25CD082-AI-ESSENTIALS.pdf` | Core IEEE workshop assignment document covering literature review, system architecture, comparison tables, and research gap. |
| `README.md` | Comprehensive project documentation and system specifications. |
| `day2-coding-assignment.md` | Reference document / problem statement URL for coding assignments. |
| `resume (1).pdf` | Student profile and credentials document. |

---

## ⚙️ Key Technical Takeaways

* **Edge Computing Efficiency**: Processing camera feeds locally at the signal pole reduces decision latency to **0.5 seconds** while keeping external data transmission minimal.
* **Cost-Performance Balance**: Edge AI infrastructure reduces network dependance compared to cloud-only solutions, offering a cost-effective alternative ($1,200 vs $2,500) with higher operational reliability.
