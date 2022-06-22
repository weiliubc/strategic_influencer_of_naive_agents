# Propositions and Payoffs

This folder contains notebooks relating to numerical analysis of propositions about the original model.

## January 2022

### [Proposition 1](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/proposition_1.html) and [Proposition 2](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/proposition_2.html)
These notebooks provide numerical simulations and verifications of propositions 1 and 2 of the basic model. The following additional graphs for proposition 1 were generated:
![image](https://user-images.githubusercontent.com/30967260/174910005-65893bea-9e94-410b-8ace-69af6ad5d1eb.png)
![image](https://user-images.githubusercontent.com/30967260/174910021-7d0dd310-2f79-4954-9bcd-a122986f4549.png)

### [Proposition 1 Variations](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/proposition_1_variations.html)
This notebook extends the previous simulation notebook for proposition 1 by varying the structure of the A matrix. The proposition stops working after an epsilon = 0.016 shock. Further investigation after this notebook revealed that this breakdown only occurs when the naive agents have initial opinions of different magnitudes.

### [Payoff Bounds](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/payoff_bounds.html)
This notebook explores computing a lower bound on the payoff for the strategic agent. Specifically, a bound constructed from first principles:
![image](https://user-images.githubusercontent.com/30967260/174911249-be659a1d-7082-43c7-a0c0-bc2731f07d74.png)
is compared to a simple bound using the payoff of the $r_t = 0$ no-strategy bound. The no-strategy bound was found to be stronger.

### [Proposition 2 Extended](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/proposition_2_extended.html)
This notebook explores an extension of proposition 2 showing convergence of the myopic strategy is faster than convergence of the simple strategy $r_t = 0$.

At this point, a handful of additional external graphs were generated:

![image](https://user-images.githubusercontent.com/30967260/174914129-1cc29951-b725-486f-bc46-2c523a51d493.png)
![image](https://user-images.githubusercontent.com/30967260/174914145-6407de80-0e73-40db-b889-af6c64e0ebe0.png)
![image](https://user-images.githubusercontent.com/30967260/174914164-c0cb6fb7-7887-4bc1-a03a-df48280ce598.png)
![image](https://user-images.githubusercontent.com/30967260/174914199-e08b135b-5274-48ee-9e15-092747e63add.png)

### [Optimal Payoff Dependency](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/optimal_payoff_dependency.html)
This notebook explores the dependency of the optimal payoff on various network factors and demonstrates that, with respect to variations of other parameters, there is no dependency on the b vector when R = 0.

### [Revision to the Above](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/optimal_payoff_dependency_steady_state.html) and [Constant B Variant](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/constant_b.html)
These two notebooks expand on the previous by, firstly, obtaining the steady-state results properly and then exploring the row sums of the K_ss matrix with respect to b and |a_ii - a_ij| in which it was found that the row sums stay constant in |a_ii - a_ij|.

### [Payoff vs B](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/propositions_and_payoffs/payoff_vs_b.html)
This notebook continues the above experiments but goes into further detail exploring the rates of change of the individual payoff terms with respect to b. The opinion cost term was found to dominate the message cost term and thus obscure the non-monotonic effect the message cost term had.
