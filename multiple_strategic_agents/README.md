# Multiple Strategic Agent Models: Competitive Influencers

This folder contains simulations relating to models with more than one strategic agent.

## July 2021

### [First Numerical Verification](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/first_numerical_verification.pdf)
This notebook provides a first test of the Bellman equations for the multiple strategic agent model. In doing so, it was identified that an additional term was needed in some of the matrices to account for non-zero agendas.

### [Multiple Agent Test Suite](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/multiple_agent_test_suite.pdf)
This notebook runs five tests to ensure correctness and compatibility with previous notebooks, followed by a series of experiments on the multiple strategic agent model. The delta = 1 case, which previously did not converge, was found to not converge here either (and was due to exclusively the kappa matrix i.e. the constant term). Strategies between the two strategic agents appeared to decrease in each other, and a limit matrix was identified.

### [Test Suite Extensions](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/test_suite_extensions.pdf)
This notebook extends a few tests from the previous one. In addition to clarifying a handful of points from the previous notebook, a distinction was made between the Nash equilibrium and the socially optimal solution of the basic two strategic agent case with a written explanation.

### [Cost Variations](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/cost_variations.pdf)
This notebook varies the R cost term of each strategic agent's messages. It was concluded that message magnitude was inversely related to message cost, and that as cost is driven towards zero, the equilibrium strategy of each strategic agent approaches the strategy of a single strategic agent in the noncompetitive model under the same parameters.
![Visual representation](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/cost_variations.gif)

## September 2021

### [Simple Benchmarks](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/simple_benchmarks.pdf)
This notebook benchmarks the multiple strategic agent model against the single strategic agent model. However, it is not a correct comparison because the influence used in the two strategic agent case was not a correct split of that used in the one strategic agent case.

### [Benchmarks with Split Influence](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/benchmarks_split_influence.pdf)
This notebook revises the above notebook to correctly split 2b = 0.3 such that b = 0.15 for each strategic agent in the two agent case. The two strategic agent case has long-term lower payoff and slower convergence but uses less intensive initial messages.

### [Benchmarks with Dual Message](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/benchmarks_dual_message.pdf)
This notebook expands on the above notebook to have the single strategic agent model produce two messages at once instead of one message at once. It turned out that using one message only is more optimal than using two, except at cost extrema where they are equally optimal. The dual strategic agent case also turned out to be better than the dual message case in the single agent model, likely due to the single agent having to take on the contrary-to-socially-optimal-solution weight of two messages. Much of these results are due to the fact that there is only one naive agent, so there may be differences if more agents are added.

At this point in time, I generated a series of graphs comparing what happened when the weights of each agent's message in the dual strategic agent case were different from each other. However, this revealed a mistake in the code that only occurs when each agent's messages have different weights (and so was not a problem before).

### [Analytical Multi-Message Verification](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/analytical_multi_message_verification.pdf)
This notebook uses SymPy to compute the solution of a simple form and example of the the dual strategic agent model which helped prove that the previous code was incorrect. There later turned out to be a small sign typo in the FOCs at the beginning which was fixed in a subsequent notebook.

### [Multi-Agent Debugging](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/multi_agent_debugging.pdf)
This notebook debugs the incorrect equations and fixes an indexing typo in doing so. One remaining issue was identified afterwards in the scaling of r_t^2 in comparison to the analytical check.

### [Analytical Multi-Message Verification (fixed)](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/analytical_multi_message_verification_fixed.pdf)
This notebook fixes the sign typo of the previous version of this notebook.

### [Analytical Dual Message Single Agent Case](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/analytical_dual_message_single_agent.pdf)
This notebook verifies that an observed slight difference in the two message one agent and one message two agent cases is expected due to the different formulations.

### [Benchmarks with Dual Message (asymmetric case)](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/benchmarks_dual_message_asymmetric.pdf)
This notebook employs the fixed code to compare the two-message one-agent case to the two-agent one-message case with asymmetric weights. We see the same conclusions as the symmetric version, and that in the two strategic agent case, the agent with the smaller weight has greater payoff and smaller messages. The same smaller messages are present in the smaller channel of the one-agent case with two messages.
