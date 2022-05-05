# Starting Point: Bot Examples

This folder contains all simulations relating to the bot extensions of the strategic influencer model. These stem from the original example with a single strategic agent and five naive agents.

## May-June 2021

### [First Experiments](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/basic_model/first_experiments.pdf)
This notebook explored the original model with respect to various finite and infinite-horizon trajectories, relating the code to the theory. After implementing setups related to the example from the paper, initial experiments were conducted for the case of "bot" agents with fixed opinions followed by different network structures. It was found that the strategic agent's messages cannot converge under the presence of stubborn agents without discounting due to fixed opinions always inducing costs; this notebook had a typo in the code that mixed the myopic strategy with the optimal strategy and so more detailed conclusions cannot be drawn from it alone. It was noted in discussions that examples and experiments for real-life networks could be used to test the theory.

Some discussion points (Wei):
- Myopic vs. optimal: for a small network, it is not easy to generate a large difference between myopic and optimal strategy, except for small horizon case. Note that the example in the slide is for T=5 (so solve for r^m and r^* when T=5 only), and the biggest difference between the two strategies occurred in period 1 and 2. The difference in the long run (so if the time is very large), is barely noticeable. I think this just means that the myopic strategy (greedy algorithm) in the long term is pretty good.
- Uniform influence: when the weights are all the same (line 20, page 12), you can prove it converges in two periods. All the agents need 1 period to form the same belief, at that point, all the agents behave as one agent. Then it takes one period for the strategic agent to get all opinions to 0.
- Superbots: there are two things. First, if agent 1 (in line 30, page 16) does not listen at all, then his opinion clearly does not change if he is a stubborn naive agent and the strategic agent cares about his opinion. As my earlier message mentioned, if the strategic agent cares about him, total cost is unbounded and this problem does not have a solution. If strategic agent does not care about agent 1, then it may be fine. I think if strategic agent does not care about bots, and if her messages are unbounded, and all naive agents listen somewhat to the strategic agents, the opinions will go to 0 (but not her messages). It will be great to know if this is correct, or there is a counterexample.

## July 2021

### [Convergence of Cycles](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/convergence_of_cycles.pdf)
This notebook explores the following matrix, which has a cyclic structure:
```
[0, 0.5, 0.5]
[0.99, 0, 0]
[0.99, 0, 0]
```
It was concluded that oscillatory behaviour in the agent opinions arises due to the presence of this cycle, but also that the presence of stubborn agents can "dampen" the oscillations and induce convergence.
