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
