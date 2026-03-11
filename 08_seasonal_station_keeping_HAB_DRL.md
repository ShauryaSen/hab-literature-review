# Seasonal Station-Keeping of Short Duration High Altitude Balloons using Deep Reinforcement Learning

**Authors:** Tristan K. Schuler, Chinthan Prasad, Georgiy Kiselev, Donald Sofge  
**Year:** 2025  
**Venue:** arXiv (U.S. Naval Research Laboratory)  
**Link:** https://arxiv.org/abs/2502.05014

This paper analyzes how HAB station keeping performance varies by season and geography. It introduces a "Forecast Score" that predicts station-keeping feasibility based on wind diversity.

---

## Motivation
Other papers don't quantify how success might be influenced by seasonal and geographic wind diversity.
## Method
1. generates high vertical resolution wind fields from historical radiosonde measurements to incorporate realistic atmospheric uncertainties into DRL training, without relying on expensive NWP runs.
2. Introduced **forecast score** algorithm to independently  classify wind diversity. Higher diversity means more options for the RL agent to exploit.
3. The agents were trained and tested across different months of the year to reveal how strongly station keeping success depends on seasonal wind patterns.
## Results
- The synthetic wind forecasts provided significantly higher vertical resolution giving 46 pressure levels vs 7 for ERA5 in the operating region. It also demonstrated realistic seasonal deviations from ERA5 reanalysis.
- Forecast score correlated strongly with DRL agent performance, higher wind diversity meant the DRL agent performed better.