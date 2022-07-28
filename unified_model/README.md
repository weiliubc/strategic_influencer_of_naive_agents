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

### [Model Cross-Comparison: Higher Cost Version](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/unified_model/higher_cost.ipynb)
This notebook implements the baseline comparison with c increased to 200. Several printouts and checks relating to the opinion values in the infinite horizon model are added.
