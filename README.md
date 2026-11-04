# Real India TSP: Hill Climbing with 2-Opt Local Search

An interactive animated visualization tool analyzing the Traveling Salesperson Problem (TSP) using Hill Climbing (Local Search) with 2-opt edge exchanges across 28 major Indian transport hubs. Distances are computed using the geodesic spherical Haversine formula in kilometers.

## 🚀 Live Demo
- **Vercel Deployment:** https://tsp-hill-climbing-visualizer.vercel.app/

## 📌 Problem & Search Formulation
- **State Space ($S$):** Complete cyclic Hamiltonian permutation connecting all selected cities.
- **Objective Function ($f(S)$):** Minimize total spherical Earth distance (km) using the Haversine equation.
- **Neighborhood / Frontier ($N(S)$):** All $\frac{n(n-1)}{2}$ candidate 2-opt edge swaps generated from the current tour.
- **Transition Policy:** Steepest ascent (best-improvement) accepting $\min(\Delta \text{Cost}) < 0$.
- **Local Optimum Convergence:** Search terminates when all candidate swaps in the neighborhood yield $\Delta \text{Cost} \ge 0$.

## ✨ Features
- **Deterministic Step Playback:** Full timeline controls (Play, Pause, Step Forward, Step Back, Reset, and scrub slider).
- **Interactive Visual Swap Highlights:** Green highlight lines showing untangled edge reconstructions.
- **Search Transparency Log:** Live telemetry detailing edges cut, edges reconnected, and delta cost per step.
- **Live Convergence Curve:** Real-time SVG tracking asymptotic distance reduction.
- **Empirical Benchmarks:** Automatic runtime, evaluation count, and improvement tracking across presets.

## 📊 Experimental Datasets
Trial logs and performance matrices are stored in the [`/data`](./data) directory:
- `TSP_Performance_Summary.csv`: Aggregated corridor benchmarks and runtimes.
- `TSP_Iteration_History.csv`: Step-by-step transition and cost delta logs.
- `TSP_Experiment_Results.csv`: Empirical convergence trials across random seeds.

## 👥 Team 12 - Contribution Breakdown
- **Role 1 (Algorithm & Local Search Logic):** Haversine geodesic matrix, 2-opt inversion logic, delta-cost minimization, local optimum convergence detection.
- **Role 2 (Visualization & Animation Engine):** HTML5 Canvas coordinate mapping, dynamic edge morphing, timeline scrub state machine.
- **Role 3 (UI/UX, Performance Analysis & Documentation):** Dark dashboard UI, benchmark logging, CSV telemetry generation, project report, and demo video.
