### Methods

#### Bayesian Optimization & Gaussian Processes

| #   | Paper                                                                         | Year | What It Does                                                                    | Key Takeaway                                                                                         |
| --- | ----------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| 1   | [Optimal Launch Sites for HABs](01_identifying_optimal_launch_sites_BO.md)    | 2024 | Uses BO+GP to find the best launch time/location for balloon station-keeping    | Best launch site is often outside the target zone. BO finds it in fewer evaluations than grid search |
| 2   | [Multi-AUV Plume Estimation](02_multi_AUV_sediment_plume_BO.md)               | 2024 | Sliding-window BO for mapping time-varying underwater plumes with multiple AUVs | The sliding-window GP that forgets stale data is applicable to changing wind fields                  |

#### Deep Reinforcement Learning

| #   | Paper                                                                            | Year | What It Does                                                                                 | Key Takeaway                                                                           |
| --- | -------------------------------------------------------------------------------- | ---- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 4   | [SAC Balloon Control](04_SAC_underactuated_balloon_control.md)                   | 2023 | SAC (continuous actions) for latex balloons with irreversible venting/ballasting              | More relevant for cheap weather balloons; adds a resource-budgeting problem            |
| 8   | [RL for Outdoor Balloon Navigation](08_RL_outdoor_balloon_navigation.md)         | 2024 | SAC trained in sim, deployed on a real balloon. 6 outdoor flights with 360m avg target error  | First real-world RL balloon navigation; sim-to-real transfer works without fine-tuning  |
| 9   | [Seasonal Station-Keeping (NRL)](09_seasonal_station_keeping_HAB_DRL.md)         | 2025 | DQN for HAB station-keeping with seasonal/geographic wind analysis + Forecast Score metric   | Forecast Score predicts RL feasibility before launch                                   |

---

### Applications

These papers demonstrate real-world uses of the above methods — or present systems where our work could have direct impact.

| #   | Paper                                                                                        | Year | Domain                | What It Demonstrates                                                                               | Why It Matters to Us                                                                                         |
| --- | -------------------------------------------------------------------------------------------- | ---- | --------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| 5   | [NASA STRATO Wildfire Monitoring](05_NASA_STRATO_wildfire_monitoring.md)                     | 2024 | Stratospheric balloon | 11-day persistent LTE + IR imaging over Idaho wildfires                                            | The strongest near-term use case for balloon station-keeping; opens the fire-tracking navigation problem      |
| 6   | [Loon Data Assimilation (NASA GEOS)](06_global_assimilation_loon_balloon_observations.md)    | 2019 | Weather forecasting   | Assimilated 3 months of Loon wind data into NASA GEOS — tropical wind errors up to 8 m/s corrected | Balloon navigation + wind sensing is dual-use: our RL/BO-navigated balloons directly improve weather forecasts |
| 7   | [Redwing Glider Circumnavigation](07_redwing_glider_circumnavigation.md)                    | 2025 | Underwater glider     | 5-year global circumnavigation exploiting major ocean currents                                     | The underwater twin of balloon navigation — same 1-DOF control, same flow exploitation, transferable methods  |

---

## References (by Paper Number)

1. Saunders et al. (2024). Identifying Optimal Launch Sites of HABs using Bayesian Optimisation. arXiv:2403.10784.
2. Multi-AUV Sediment Plume Estimation using BO (2024). Frontiers in Marine Science.
4. Resource-Constrained Station-Keeping for Helium Balloons using RL (2023). arXiv:2303.01173.
5. NASA STRATO Program (2024). Armstrong Flight Research Center / Aerostar.
6. Coy, Schoeberl, Pawson, et al. (2019). Global Assimilation of Loon Stratospheric Balloon Observations. J. Geophys. Res. Atmos., 124(6), 3005–3019.
7. Redwing Glider Sentinel Mission (2025). Rutgers/Teledyne Marine.
8. Jeger, Lawrance, Achermann, Pang, Kovac, Siegwart (2024). Reinforcement Learning for Outdoor Balloon Navigation. IEEE Robotics & Automation Magazine. DOI: 10.1109/MRA.2023.3271203.
9. Schuler, Prasad, Kiselev, Sofge (2025). Seasonal Station-Keeping of Short Duration High Altitude Balloons using Deep Reinforcement Learning. arXiv:2502.04748.
