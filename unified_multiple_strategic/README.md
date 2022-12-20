TODO: move some notebooks from the baseline unified model into this folder

## October 2022

### [Different Agendas: K^* printouts](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_different_agenda_K.ipynb)
This notebook provides code for the infinite-horizon $K^*$ and some printouts under the symmetric network case.

## November 2022

### [Full General Model](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_old_revised.ipynb)
This notebook upgrades the old multiple strategic agents general code to work with the unified model. Results are preliminary and outlined inside. The results from the symmetric cases continue to hold with this model.

### [Asymmetric Network Analysis](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_asymmetric_analysis.ipynb)
This notebook provides some printouts comparing steady-state matrices and limit opinions of symmetric and asymmetric networks under otherwise identical setups. The limit opinions in both cases, given two strategic agents with one agenda set to zero, appears to be the average of the two agendas. The element sum of each $k^*$ appears to be linear in the two agendas with equal but opposite coefficients and zero-intercepts.

### [Message Weights](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_weighted_messages.ipynb)
This notebook tests adding a specific weight $a_i$ to the message of each strategic agent. In the general case, the limit opinions appear to now depend on the network $A$ as well as $\delta$ and $c$. As $a_i$ is brought to infinity, the agenda $b_i$ becomes the limit opinions; if brought to zero, the opposite agenda $b_{-i}$ becomes the limit; if the $a$ weights are the same, the limit opinions take the usual average of agendas form (except in limit cases; if they are both zero, the limit opinions are the network evolution without the strategic agents, and if they are both infinity, something unknown but different happens due to it being impossible to fully compute). There is an odd anomaly where under some conditions on $A$ and $\delta$, one of the limit opinions first increases in $a_2$ before decreasing to get to the limit $b_2$.

### [Message Weights Symmetric Case with Opposite Agendas](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_weighted_symmetric.ipynb) and [Offset Agendas](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_weighted_symmetric_agenda_offset.ipynb)
The above notebook but repeated for a symmetric, stubborn network with agenda pairs (-5, 5) and (0, 5), respectively. K still appears to be different whenever the a_i are different. Graphs are included for comparative statics with respect to a_1, delta, c and x_0.

## December 2022

### [Convergence Analysis w.r.t. Numerical Error: Experimentation](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_weighted_scaled_up.ipynb)
This notebook provides some test cases that demonstrate how apparent convergence may or may not actually be convergence after accounting for the "propagation" effect of numerical error.

This is not included in the notebook but the command `run_simulation(-2000000, 500000, 0.5, 0.6, c = 0.001)` was able to produce a result with significantly different limit opinions: -357k, -413k and -382k approximately.

[Here](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_weighted_scaled_up_rough_copy.ipynb) is a rougher version with more results (but no annotation on the new results and code blocks run out of order).
