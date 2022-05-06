# Starting Point: Bot Examples

This folder contains all simulations relating to the bot extensions of the strategic influencer model. These stem from the original example with a single strategic agent and five naive agents.

## May 2021

### [First Experiments](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/basic_model/first_experiments.pdf)
This notebook explored the original model with respect to various finite and infinite-horizon trajectories, relating the code to the theory. After implementing setups related to the example from the paper, initial experiments were conducted for the case of "bot" agents with fixed opinions followed by different network structures. It was found that the strategic agent's messages cannot converge under the presence of stubborn agents without discounting due to fixed opinions always inducing costs; this notebook had a typo in the code that mixed the myopic strategy with the optimal strategy and so more detailed conclusions cannot be drawn from it alone. It was noted in discussions that examples and experiments for real-life networks could be used to test the theory.

Some discussion points (Wei):
- Myopic vs. optimal: for a small network, it is not easy to generate a large difference between myopic and optimal strategy, except for small horizon case. Note that the example in the slide is for T=5 (so solve for r^m and r^* when T=5 only), and the biggest difference between the two strategies occurred in period 1 and 2. The difference in the long run (so if the time is very large), is barely noticeable. I think this just means that the myopic strategy (greedy algorithm) in the long term is pretty good.
- Uniform influence: when the weights are all the same (line 20, page 12), you can prove it converges in two periods. All the agents need 1 period to form the same belief, at that point, all the agents behave as one agent. Then it takes one period for the strategic agent to get all opinions to 0.
- Superbots: there are two things. First, if agent 1 (in line 30, page 16) does not listen at all, then his opinion clearly does not change if he is a stubborn naive agent and the strategic agent cares about his opinion. As my earlier message mentioned, if the strategic agent cares about him, total cost is unbounded and this problem does not have a solution. If strategic agent does not care about agent 1, then it may be fine. I think if strategic agent does not care about bots, and if her messages are unbounded, and all naive agents listen somewhat to the strategic agents, the opinions will go to 0 (but not her messages). It will be great to know if this is correct, or there is a counterexample.

## June 2021

### [Bot as Sixth Agent](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/bot_as_sixth_agent.pdf)
This notebook implements some improvements to the modification of the model for having a "bot" agent; notably, the bot is added as an additional naive agent and excluded from the opinion cost term so as to preserve the state of the original network for comparison purposes. This notebook still contains the strategy code typo as mentioned above, though it was possible to conclude that the presence of bots prevents all naive agents from converging to exactly the strategic agent's agenda, though they do converge somewhere.

### [Bot Convergence Tests](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/bot_convergence_tests.pdf)
This notebook implements the fix to the code that initially caused the optimal solution to appear like the myopic solution (this turned out to be due to an incorrectly transposed B vector). This notebook explores convergence of opinions in bot networks with various values of delta, most cases which demonstrated convergence to a point away from the strategic agent's agenda. "Tail" structures were observed in some plots of messages where convergence of messages to a nonzero point trended towards zero at the very end; this turned out to be due to using finite-horizon solutions instead of steady-state infinite-horizon solutions.

### [Limit Matrix Eigenvectors](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/limit_matrix_eigenvectors.pdf)
This notebook, in addition to using the proper steady-state matrices for infinite-horizon models from above, explores the limiting matrix (\tilde A+\tilde BL_{ss})^t as t goes to infinity. Most of this matrix converges to zero (due to the influence of the bot being dominant over the other naive agents), except the column with the same index as the bot, which has values exactly 1/10th of the steady-state opinions. This 10 arises from the choice of initial opinion for the bot.

### [Strategic Limit Influence](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/strategic_limit_influence.pdf)
This notebook adds the strategic agent as a "seventh naive agent" to the model to compute limit influence in the way limit influence was computed for the bot agent above. Two approaches were found and, unlike above, the matrix is stochastic (rows sum up to 1 so all influence is accounted for). It was also concluded that each individual message broadcasted by the strategic agent has a diminishing and finite influence over the naive agents as it propagates through a particular network, due to the presence of simultaneous "messages" generated by the bot's influence, which is why the strategic agent's messages do not always converge to zero as her own messages do not sustain permanently among the naive agents.

## July 2021

### [Opinions vs Agenda Distance](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/opinions_vs_agenda_distance.pdf)
This notebook explores the formulation of the naive agent limit opinions as a function of the distance between the agendas of the bot and strategic agent. It was concluded that a linear relationship is present between the opinions and each of the two individual agendas.

### [Steady-State vs Optimal](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/steady_state_vs_optimal.pdf)
This notebook addresses the issue that when adding the strategic agent as a seventh agent to the network, r_ss is used as her opinion instead of the true sequence of r_t. This notebook compares the two sequences in terms of limits and convergence, which was found to only differ in the short-run as both sequences converge to r_ss in the long-run. Convergence time for purely using r_ss as the messages each period was found to be much worse than using the true r_t for each t.

### [Convergence of Cycles](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/bots/convergence_of_cycles.pdf)
This notebook explores the following matrix, which has a cyclic structure:
```
[0, 0.5, 0.5]
[0.99, 0, 0]
[0.99, 0, 0]
```
It was concluded that oscillatory behaviour in the agent opinions arises due to the presence of this cycle, but also that the presence of stubborn agents can "dampen" the oscillations and induce convergence.
