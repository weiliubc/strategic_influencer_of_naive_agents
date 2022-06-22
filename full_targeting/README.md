# Full-Length Targeting Models

This folder contains notebooks relating to the original targeting models.

## October 2021

### [Basic Example](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/basic_example.pdf)
This notebook was a quick check of the targeting model with stubborn and easily-influenced naive agents. Targeting the stubborn agent was found to be more optimal. This notebook also set the choice of reweighting the strategic agent's influence between the two naive agents to be a simple weighted average of the existing A matrix row and the influence weight of the strategic agent.

### Symbolic Targeting Solution: [first agent](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/symbolic/symbolic_target_first.pdf) and [second agent](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/symbolic/symbolic_target_second.pdf)
These notebooks, hosted in the symbolic folder, were a first try at symbolically solving the targeting model. At this point in time, the expressions were too complex to interpret.

### [Symbolic Targeting and Cost Analysis](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/symbolic/symbolic_targeting_and_cost_analysis.pdf)
This notebook, hosted in the symbolic folder, improves some of the symbolic equations from above. After doing so, it explores robustness of the K matrices in the targeting model with respect to message costs and duplicate naive agents.

### [Short Term Analysis](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/short_term.pdf)
This notebook compares targeting strategies in the short term. It also explores the behaviour of the individual entries of the K matrix, which appear to be decreasing with time.

### Targeting with Cost: [Stubborn](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_with_cost_stubborn.html) and [Easygoing](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_with_cost_easygoing.html) Agents
These two notebooks provide comparative statics on the targeting model with respect to R and delta. The basic tagreting results from before are sustained.

### Myopic vs Optimal Strategy in Targeting: [Stubborn](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_myopic_vs_optimal_stubborn.html) and [Easygoing](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_myopic_vs_optimal_easygoing.html) Agents
These notebooks compare the myopic and optimal strategies in the targeting model. The strategies become similar to each other as cost increases, but the optimal strategy is more aggressive in magnitude when cost is closer to zero.

## February 2022

### [Opinion Leader vs Stubborn Agent](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/opinion_leader_vs_stubborn.html)
This notebook explores the concept of an opinion leader agent whom every other agent listens to. It was found that targeting the stubborn agent still performs better.

### [Opinion Leader vs Stubborn Agent Extended](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/opinion_leader_vs_stubborn_extended.html)
This notebook addresses an issue with the above where the magnitude of the self-weight of the stubborn agent in A was too high compared to that of the opinion leader. It was found that the initial opinions x_0 partly determined the optimal target.

### [Bigger Network](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/bigger_network.html)
This notebook provides printouts for a bigger network under the above model.

### [Zoomed In](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/zoomed_in.html)
This notebook extensively explores the opinions and convergence rates of the above model to demonstrate how the initial opinions x_0 affect the optimality of the choice of targeted agent.

### [Standalone Opinion Leader](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/standalone_opinion_leader.html)
This notebook explores the opinion leader model with no stubborn agent. A numerical and a symbolic exercise are used to demonstrate that targeting the opinion leader instead of the opinion follower yields greater payoff. The same exercise is conducted in higher dimensions in [Standalone Opinion Leader Highdimensional](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/standalone_opinion_leader_highdimensional.html). Verification of a formula for the highdimensional case is in [Formula for Highdimensional](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/formula_for_highdimensional.html).

## March 2022

### [Comparative Statics](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_comparative_statics.html)
This notebook compares the targeting model under low-delta, high-T networks with high-delta, low-T networks to see if a short-horizon is similar to a heavily-discounted long-horizon. This was found to be true.
This notebook has an issue with finite-horizon terminal payoff; this was corrected in [this notebook](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/revised_comparative_statics.html).

### [Equal Columns](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_equal_columns.html)
This notebook checks a model with uniform columns instead of the opinion leader vs stubborn setup. Given the matrix, the optimal target depended on the column weight irrespective of delta. The same code was run under the original setup in [Equal Columns with Old Setup](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/targeting_equal_columns_old_A.html).
This notebook has an issue with finite-horizon terminal payoff; this was corrected in [this notebook](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/revised_equal_columns.html) for the base model and [this notebook](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/revised_equal_columns_old_A.html) for the older A matrix.

### [Short Horizon Test](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/test_short_horizon.html)
This notebook tests the setup under a short horizon to ensure indices are correct.

### [Relevance of Delta](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/relevance_of_delta.html)
This notebook demonstrates that the optimal target may change if delta changes. A control check with different initial opinions is in [this notebook](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/relevance_of_delta_control_check.html).

Further tests were done [here (0, 0, 20 opinions)](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/steady_state_relevance_of_delta.html), [here (more payoffs vs delta)](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/steady_state_weight.html), and [here (further analysis of 0, 0, 20)](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/zero_zero_twenty_model.html), which together indicate that the initial opinions factor into the payoff in a manner independent of delta. Plots for the 0, 0, 20 case can be found [here](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/zero_zero_twenty_model_plots.html).
![image](https://user-images.githubusercontent.com/30967260/174924587-484a7519-cad2-40e1-a500-e5a1c08666d9.png)

### [Large Network Statics](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/large_network_statics.html)
This notebook explores comparative statics with respect to x_0, delta and where the optimal target changes with a_11. Printouts are included. 

### [Large Network Statics: Limiting Case of a_11](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/larger_network_statics_x0.html)
This notebook explores the limiting case of a_11 and adjusts x_0 a bit. It was found that targeting agent 2 is only better for a certain interval of a_11.

### [Large Network Statics: Convergence](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/larger_network_statics_convergence.html)
This notebook plots the a_11 limiting case. 

### [Large Network Statics: R](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/full_targeting/larger_network_statics_R.html)
This notebook explores the model with R = 1. The result is similar but the cutoff for targeting agent 1 to be optimal with respect to a_11 is lower.
