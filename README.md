# Literature Review: Autonomous Navigation of Underactuated Vehicles

A structured literature review of methods and applications for navigating underactuated systems — with a primary focus on **stratospheric hot-air balloon navigation using reinforcement learning** and a secondary focus on analogous underwater systems.

## Overview

This review covers **8 papers** across two themes:

### Methods — *How do underactuated vehicles navigate?*

| # | Paper | Method | Year |
|---|-------|--------|------|
| 1 | [Optimal Launch Sites for HABs](01_identifying_optimal_launch_sites_BO.md) | Bayesian Optimization + GP | 2024 |
| 2 | [Multi-AUV Plume Estimation](02_multi_AUV_sediment_plume_BO.md) | Sliding-Window BO + TSP | 2024 |
| 4 | [SAC Balloon Control](04_SAC_underactuated_balloon_control.md) | Soft Actor-Critic (continuous RL) | 2023 |
| 8 | [RL for Outdoor Balloon Navigation](08_RL_outdoor_balloon_navigation.md) | SAC (sim-to-real transfer) | 2024 |
| 9 | [Seasonal Station-Keeping (NRL)](09_seasonal_station_keeping_HAB_DRL.md) | DQN + Forecast Score metric | 2025 |

### Applications — *Where are these methods used?*

| # | Paper | Domain | Year |
|---|-------|--------|------|
| 5 | [NASA STRATO Wildfire Monitoring](05_NASA_STRATO_wildfire_monitoring.md) | Stratospheric balloon | 2024 |
| 6 | [Loon Data Assimilation (NASA GEOS)](06_global_assimilation_loon_balloon_observations.md) | Weather forecasting | 2019 |
| 7 | [Redwing Glider Circumnavigation](07_redwing_glider_circumnavigation.md) | Underwater glider | 2025 |

## Detailed Summary

For a detailed comparison of all papers with key takeaways, see the **[Papers Overview](Papers%20Overview.md)**.

## Approach

Each paper was analyzed using a structured template covering:
- **Core Methodology** — the algorithm or technique used
- **Motivation** — the problem being addressed
- **Primary Advantage** — specific performance metrics or key results

---

*Click any paper title above to read the full review.*
