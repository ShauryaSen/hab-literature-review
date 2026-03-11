# Multi-AUV Sediment Plume Estimation using Bayesian Optimization

**Year:** 2024  
**Venue:** Frontiers in Marine Science  
**Link:** [Frontiers](https://www.frontiersin.org/journals/marine-science/articles/10.3389/fmars.2024.1504099/full)

This paper uses Bayesian Optimization to map a time-varying field you can't see all at once. Their key innovation is a "sliding-window" BO that forgets old measurements as conditions change which could translate to changing wind fields. They also combine BO with a Traveling Salesman solver to make multi-vehicle sampling efficient -> perhaps multi baloon coordination could be useful.

---

## Core Methodology
**Distributed Bayesian Optimization (BO) using Gaussian Process Regression (GPR)** with a Sliding-Window Upper Confidence Bound (SW-UCB) acquisition function, combined with a Traveling Salesman Problem (TSP) solver for efficient multi-AUV path planning.

The approach works as follows:
1. **GP Surrogate Model:** A Gaussian Process models the unknown suspended particulate matter (SPM) concentration field using a kernel function that captures spatial correlations.
2. **Sliding-Window BO (SW-UCB):** To handle the time-varying nature of sediment plumes, only the last `l_win` measurements are retained in the GP older measurements are discarded via a sliding window. This prevents the GP from being fit to stale data while capping computational cost.
3. **Drift Model:** Measurements are artificially "moved" with the estimated water current to account for plume advection between sampling times.
4. **TSP Path Optimization:** Instead of sampling one point per BO iteration, the top *N_TSP* candidate locations (based on UCB values) are selected, and the shortest route through them is computed using the Held-Karp algorithm. This batched approach greatly increases sampling efficiency for distance-constrained AUVs.
5. **Split-Path Method:** Additional sample points are interpolated along the TSP path, providing opportunistic measurements between planned waypoints.
6. **Domain Reduction:** A dynamic bounding box tracks the plume extent to avoid wasting AUV time sampling empty regions.

---

## Primary Advantage
**The BO+TSP approach monitors time-varying sediment plumes with good overall estimation error** across 3D space and time, even with limited AUVs. The sliding-window mechanism prevents GP model degradation as the plume evolves. The authors demonstrate successful plume tracking over a 16-hour simulated dredge experiment.

The method is shown to correctly estimate the rough shape and concentration of the plume at all time steps, with the largest errors occurring at the domain boundary where the plume enters and where turbulence is highest.
