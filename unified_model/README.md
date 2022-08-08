This folder contains results relating to the unified model.

## July 2022

### [Equation Test](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/equation_test.ipynb)
This notebook does a quick check of the convergence rates for the naive agent opinions and finds that they are increasing in the corresponding eigenvalue of A.

### [Equation Test: Ratio](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/equation_test_ratio.ipynb)
This notebook tries the above procedure with the expression $K_j^* / \lambda_j$ instead. It turns out that this expression is not monotone in $\lambda_j$.

### [Equation Test: Ratio Reciprocal](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/equation_test_ratio_2.ipynb)
This notebook is the above notebook but with analysis on $\lambda_j / K_j^*$, the reciprocal of the above expression. The same result is observed as the previous notebook.

### [Equation Test: Derivatives](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/equation_test_derivatives.ipynb)
This notebook prints out the derivatives of the expressions created when going from the ratio approach to the direct convergence rate approach.

### [Model Cross-Comparison](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/model_cross_comparison.ipynb)
This notebook compares the model to no-intervention and one-shot-intervention models. The unified model has higher payoff than both and converges faster than the no-intervention model (convergence speed is more ambiguous in comparison to the one-shot model but accuracy to agenda is higher in the unified model). In addition, the network with a smaller second-highest eigenvalue was found to converge faster and give higher payoff than the network with a larger second-highest eigenvalue (i.e. one with a stubborn agent).

### [Model Cross-Comparison: Extra Plots](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/extra_plots.ipynb)
This notebook implements the above notebook but presents the projected opinions and messages (whereas the above presents the unprojected opinions and messages).

### [Model Cross-Comparison: Higher Cost Version](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/higher_cost_version.ipynb)
This notebook implements the baseline comparison with c increased to 200. Several printouts and checks relating to the opinion values in the infinite horizon model are added.

### Convergence Speed Analysis: [Projected](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/convergence_speed_analysis.ipynb) and [Unprojected](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/convergence_speed_analysis_unprojected.ipynb) Versions
These two notebooks provide analysis of convergence speed in the model. It was observed that opinions in balanced networks visually converge to zero faster than those in stubborn networks only with the projected opinions. A check for correctness using the analytic opinion expression in comparison to the recursive numerical approach was also created.

### [Convergence Speed Analysis with Higher a_11](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/convergence_speed_analysis_3.ipynb)
This notebook displays the plots of projected opinions for a more stubborn network, which appears to continue to show faster convergence in the more balanced network case.

### [Myopic Comparison](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/myopic_comparison.ipynb)
This notebook compares the myopic strategy to the one-shot strategy for a small horizon. Opinions are able to get closer to the target agenda under the one-shot strategy here, but this comes at higher cost and so the payoff is worse under one-shot compared to myopic.

The above notebook had a typo in that the one-shot model used the infinite-horizon solution instead of the finite-horizon solution, which is corrected [in this revised notebook](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/myopic_comparison_revised.ipynb). The same conclusions as previous still hold despite the change.

## August 2022

### [Small Delta Myopic Comparison](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/myopic_comparison_small_delta.ipynb)
This notebook repeats the exercise for a longer finite horizon and a smaller value of delta. The limiting behaviour for decreasing delta is that the two models approach equality but the myopic payoff is always above the one-shot payoff.

### [Limit with Bots](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/limit_with_bots.ipynb)
This notebook explores an extension where a "bot" with fixed agenda/messages influences the naive agents using the same mechanics as the strategic agent in every period. In the examples so far, the naive agent opinions always converge to some point. As a baseline, the strategic agent can always do at least as good as counteracting the bot perfectly in each period, which will leave the naive agents to converge on their own (if a limit exists). The strategic agent can also do as least as good as counteracting the bot perfectly and, on top of this, adding the messages required for the naive agents to converge as if the bot did not exist.

### [Myopic vs One-Shot: Finite-Horizon Proof](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/payoff_comparison_test_finite_proof.ipynb)
This notebook attempts to prove that the myopic strategy has strictly higher payoff than the one-shot strategy for finite-horizons of $T = 2$ and above given nonzero parameters (otherwise we have only weakly higher payoff). A proof by induction is used.
