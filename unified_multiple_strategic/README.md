## October 2022

### Notebooks from other folder

### [Unified Model with Multiple Strategic Agents: Fully Symmetric Case](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_model/multiple_unified_symmetric.ipynb)
This notebook provides an initial test of the unified model version of the multiple strategic agent model. Only the symmetric case i.e. symmetric and Markov network combined with symmetric strategic agents having zero-level agendas is covered so far. It was observed that, for the tested matrix, an increase in $L$ causes a decrease in the absolute values of opinions and optimal messages. This is robust with respect to increases in $c$, at least for the tested increase.

### [Unified Model with Multiple Strategic Agents: Symmetric Finite-Horizon Analysis](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_model/mus_finite.ipynb)
This notebook prints out the resulting finite-horizon $K_t$, $MK_t$ and $L_t$ for various values of the number of strategic agents $M$, including for approaching the upper limiting case. Periodicity in $K_t$, $MK_t$ and $L_t$ begins to occur from $M = 3$ upwards.

### [Unified Model with Multiple Strategic Agents: Unfinished Symmetric Finite-Horizon Induction Proof](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_model/mus_finite_induction.ipynb)
An unfinished attempt at showing $K_t$ is decreasing in $M$ and $MK_t$ is increasing in $M$.

### Notebooks in this folder

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

### [Examples for Finite T](https://github.com/weiliubc/strategic_influencer_of_naive_agents/blob/main/unified_multiple_strategic/mus_finite_examples.ipynb)
This notebook contains two examples for the symmetric finite horizon case: a shorter horizon and two 3x3 networks, all of which exhibit periodicity in the K matrices.
