# Resource-Constrained Station-Keeping for Helium Balloons using Reinforcement Learning

**Year:** 2023  
**Venue:** arXiv:2303.01173  
**Link:** [arXiv](https://arxiv.org/abs/2303.01173)

This paper uses Soft Actor-critic for continuous altitude control to enable smoother trajectory transitions and considers resource management since ballasting and venting is irreversible. It's not that interesting, it just demonstrates that SAC also works which might be unsurprising.

---
## Motivation
- High altitude balloons have severe weight and power constraints.
- Previous RL methods haven't addressed resource constrained systems.
## Core Methodology
- A Soft Actor-Critic (SAC) reinforcement learning agent was trained using a 74-feature state vector (including wind fields and balloon conditions) and a continuous 3-dimensional action space for desired altitude, urgency (time-factor), and a float override.
- A reward function was designed to maximize time within a 50km target region while explicitly penalizing resource consumption, complemented by a low-level altitude controller translating high-level SAC outputs into physically constrained venting/ballasting actions.
