# Identifying Optimal Launch Sites of High-Altitude Latex-Balloons using Bayesian Optimisation for the Task of Station-Keeping

**Authors:** Jack Saunders, Sajad Saeedi, Adam Hartshorne, Binbin Xu, Özgür Şimşek, Alan Hunter, Wenbin Li  
**Year:** 2024  
**Venue:** arXiv:2403.10784  
**Link:** [arXiv](https://arxiv.org/abs/2403.10784)

This paper uses Bayesian Optimization and GP to discover the most optimal balloon launch location which they found it often not inside the target zone. The BO/GP layer sits on top of an RL controller so its a good example of how those can be used together.

---
## Core Methodology
**Bayesian Optimization (BO) with Gaussian Process (GP) surrogate models**, combined with a Reinforcement Learning (RL) station-keeping controller.

The paper addresses a two-level optimization problem:
1. **Inner loop:** An RL-based controller (used as a black-box) performs station-keeping by adjusting the balloon's altitude to catch favorable wind layers.
2. **Outer loop:** Bayesian Optimization searches over the launch parameter space (time, latitude, longitude) to find the configuration that maximizes the expected undiscounted return from the RL controller's rollout.

The GP serves as a surrogate model of the "launch quality function" — mapping launch configurations to expected station-keeping performance. The Expected Improvement (EI) acquisition function guides the search toward promising regions of launch parameter space.

---
## Primary Advantage
> **BO finds optimal launch locations in significantly fewer evaluations than grid search or random search.** The method discovers that, surprisingly, the most optimal launch location is frequently **not within the target station-keeping zone** it is offset to exploit wind corridors that carry the balloon into the region.

The reward compensation mechanism also improved station-keeping performance on unseen weather patterns compared to vanilla RL controllers.
