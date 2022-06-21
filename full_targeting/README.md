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
These two notebooks provide comparative statics on the targeting model with respect to $R$ and $\delta$. The basic tagreting results from before are sustained.
