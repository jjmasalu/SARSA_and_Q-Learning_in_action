# SARSA_and_Q-Learning_in_action
==================================

**Reinforcement Learning Algorithms: SARSA and Q-Learning**
---------------------------------------------------------

This project provides a video implementation/explanation of two popular model-free reinforcement learning algorithms: SARSA and Q-Learning. Both algorithms are used to find the optimal policy in a Markov Decision Process (MDP).

**Getting started**
------------------
To view a video implementation of the algorithms in work, download the video file in the project

**Background**
-------------

Both SARSA and Q-Learning maintain a Q-table, Q(s, a), where each state-action pair has an associated value estimating the expected future reward from taking action a in state s.

**Algorithms**
-------------

### Q-Learning (Off-Policy)

Q-Learning learns the optimal policy regardless of the agent’s actions—it assumes the agent will always act optimally in the future.

* Update Rule: `Q(s, a) ← Q(s, a) + α [r + γ * max(Q(s', a')) - Q(s, a)]`
* Key Point: Chooses the best action (max(Q(s', a'))) regardless of what action was actually taken
* Off-policy: Learns about the greedy policy, not necessarily the one the agent is following

### SARSA (On-Policy)

SARSA updates its Q-values based on the action actually taken by the current policy.

* Update Rule: `Q(s, a) ← Q(s, a) + α [r + γ * Q(s', a') - Q(s, a)]`
* Key Point: Updates based on the behavior policy (which may include exploration)
* On-policy: Learns the value of the policy being followed, including ε-greedy

**Comparison**
-------------

| Feature | SARSA | Q-Learning |
| --- | --- | --- |
| Type | On-policy | Off-policy |
| Target | Q(s', a') (actual) | max(Q(s', a')) (greedy) |
| Policy | Learns current policy | Learns optimal policy |
| Stability | Safer with exploration | Can be more aggressive |
| Use Case | Safer in noisy/stochastic environments | Faster convergence in deterministic environments |



**Example Use Cases**
--------------------

* Finding the fastest route home (analogy)
* Solving a Markov Decision Process (MDP)

