# Reinforcement Learning for Outdoor Balloon Navigation

**Authors:** Simon L. Jeger, Nicholas Lawrance, Florian Achermann, Oscar Pang, Mirko Kovac, Roland Y. Siegwart  
**Year:** 2024  
**Venue:** IEEE Robotics & Automation Magazine  
**Link:** [IEEE](https://doi.org/10.1109/MRA.2023.3271203)

This paper demonstrates a recent success in balloon navigation using RL. A SAC agent navigates between 3D target positions by commanding altitude changes in dynamic wind fields, using both local measurements and NWP forecasts as input. Across 6 outdoor flights, the system achieved an average target error of 360m after ~10km of travel.

---

## Core Methodology
**Soft Actor-Critic (SAC) for 3D point-to-point balloon navigation**, trained in simulation and deployed on a custom autonomous balloon prototype.
- Uses the Soft Actor-Critic (SAC) algorithm to train a control policy.
- The agent navigates by processing local in-situ measurements combined with global wind predictions from large-scale Numerical Weather Prediction (NWP) models.
- The policy outputs target altitudes to exploit different wind currents at various elevations to reach a 3D destination.