
# Connecting Martingale Optimal Transport, Reinforcement Learning, and Dynamic Hedging

This document explores the deep connections between **Martingale Optimal Transport (MOT)**, **Reinforcement Learning (RL)** frameworks, and **Dynamic Hedging** strategies. It highlights how entropic regularization and actor-critic methods from RL naturally provide solutions to MOT problems, drawing connections to the **Schrödinger Bridge Problem (SBP)**.

## Key Components

### 1. Martingale Optimal Transport (MOT)
- Seeks a coupling \( \pi(x, y) \) minimizing a cost function under martingale constraints \( \mathbb{E}[Y|X] = X \).
- Introduces dynamics with time-evolving measures \( \rho_t \) and velocity fields \( v_t \) obeying the continuity equation.
- Entropic regularization is applied for computational tractability using KL divergence.

### 2. Reinforcement Learning Framework
- MOT is formulated as a Markov Decision Process (MDP):
  - **States:** Market and portfolio conditions.
  - **Actions:** Trading/hedging decisions.
  - **Rewards:** Returns adjusted by transaction costs and risk.
- Value functions can be risk-neutral or risk-sensitive.

### 3. Actor-Critic Method for MOT
- Splits optimization into:
  - **Actor:** Parameterizes and updates policy \( \pi_\theta(a|s) \).
  - **Critic:** Estimates the value \( V(s) \) or action-value \( Q(s, a) \).
- Employs policy gradients for learning.

### 4. Schrödinger Bridge Problem (SBP)
- Seeks the most probable stochastic process connecting \( \mu_0 \) to \( \mu_T \) by minimizing relative entropy.
- Equivalent to entropic OT with dynamic reinterpretation.

### 5. Unified Framework
- Demonstrates a shared information-theoretic identity:
  \[
  H(\text{Solution}\|\text{Reference}) = H(\text{Solution}\|\text{Calibration}) + H(\text{Calibration}\|\text{Reference})
  \]
- Unifies MOT, SBP, and RL under a regularization-based decomposition.

## Conclusion
This synthesis provides a robust, unified framework for tackling complex stochastic control and transport problems, with significant implications in finance and probabilistic modeling.

📄 [Download the full document](MOT_Reinforcement.pdf)
