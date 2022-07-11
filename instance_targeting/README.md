# Targeting using one message only

This folder contains notebooks regarding the model in which a strategic agent sends just one message in the initial period and lets naive agent opinions converge on their own for subsequent periods.

## May 2022

### [Singular-Instance Targeting Example](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/instance_targeting/instance_targeting.ipynb) 
This notebook explores the model via several comparative statics exercises. Notably, a unique optimal r message appears to be linear in individual initial opinions (among other factors), and the optimal agent to target also depends on the individual initial opinions. Also notable is that the model performs worse than the original per-period targeting model for all of the cases checked with respect to initial opinions and delta. The A matrix in question was:
```
[0.7, 0.3]
[0.5, 0.5]
```

### [Singular-Instance Targeting with a Stubborn Agent](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/instance_targeting/instance_targeting_stubborn.ipynb)
This notebook is the exact same as the above one except the A matrix is replaced with:
```
[0.99, 0.01]
[0.5, 0.5]
```
which generates a stubborn agent like in the original simulations. All the results found in the previous notebook hold in this one except for the fact that r has a maximum in delta instead of continuously increasing in delta.

## July 2022

### [One-Message Model with Diagonalizable A](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/instance_targeting/one_message_diagonalized.ipynb)
This notebook takes a component the symmetric version of the payoff FOC and generalizes it for any diagonalizable network matrix A instead of only symmetric matrices. An elementwise analytical solution is found for the resulting infinite sum.
