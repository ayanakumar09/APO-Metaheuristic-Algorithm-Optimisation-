# APO-Metaheuristic-Algorithm-Optimisation

## Overview
An adaptive metaheuristic algorithm inspired by Arctic puffin behavior, optimized for high performance on the CEC 2017 benchmark suite. Developed in early 2024, APO combines strategies from SMA, GTO, and PSO to effectively balance exploration and exploitation.

---

## Components

### What is a Metaheuristic Algorithm?
Metaheuristics are high-level optimization methods used for solving complex problems. They work without requiring gradient information or strict assumptions and use intelligent strategies (e.g., population-based or swarm-inspired behavior) to navigate solution spaces and find near-optimal results.

### What is APO?
Arctic Puffin Optimization (APO) is a novel metaheuristic algorithm introduced in February 2024. It is based on the foraging behavior of Arctic puffins and incorporates adaptive search dynamics. APO includes innovations inspired by existing algorithms like the Slime Mould Algorithm (SMA), Generalized Thermal Optimization (GTO), and Particle Swarm Optimization (PSO) to improve convergence behavior and solution quality.

### What is the CEC 2017 Benchmark?
The CEC 2017 benchmark is a standardized set of 30 complex optimization test functions. It is commonly used to evaluate the performance of metaheuristic algorithms across a range of problem types, including multimodal, hybrid, and composite functions. It serves as a rigorous testbed for benchmarking performance in terms of accuracy, robustness, and convergence speed.

---

## Initial Implementation
The base version of the APO algorithm modeled puffin movement in a search space using simple behavior rules. While initial results were competitive, performance on several functions revealed weaknesses in early-stage exploration and convergence toward global optima.

---

## Optimization Enhancements

### 1. Levy Flight Dynamic Step Size
Inspired by SMA and GTO, the step size decreases inversely with the number of iterations. This design enables wide exploration early in the process and more precise, focused search in later stages.

### 2. Synergy Factor (F)
Implemented as a linearly decreasing function (from 0.5 to 0.1), this factor facilitates a smooth transition from exploration to exploitation. It mimics the oscillatory behavior found in SMA to improve solution refinement over time.

### 3. Behavioral Conversion Factor (B)
A non-linear, exponentially decaying factor influenced by GTO’s cooling schedule. It accelerates the algorithm's shift from broad search behavior to local fine-tuning, promoting faster convergence.

### 4. Chaotic Initialization
The initial population is distributed using the Logistic Map, a well-known chaotic function. This improves diversity in starting positions, reducing the likelihood of premature convergence and enhancing initial exploration capabilities.

---

## Results Summary

Performance on the CEC 2017 benchmark showed significant improvements over the baseline in most functions. Selected results:

- f11: 1150 vs 12000 (base)
- f13: 2,281 vs 11300 (base)
- f18: 1200 vs 38500 (base)
- f10 : 2281 vs 4650 (base)

These results reflect improved global search ability and more efficient convergence.

