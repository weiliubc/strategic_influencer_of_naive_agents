# Multiple Strategic Agent Models: Competitive Influencers

This folder contains simulations relating to models with more than one strategic agent.

## July 2021

[First Numerical Verification](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/first_numerical_verification.pdf)
This notebook provides a first test of the Bellman equations for the multiple strategic agent model. In doing so, it was identified that an additional term was needed in some of the matrices to account for non-zero agendas.

[Multiple Agent Test Suite](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/multiple_strategic_agents/multiple_agent_test_suite.pdf)
This notebook runs five tests to ensure correctness and compatibility with previous notebooks, followed by a series of experiments on the multiple strategic agent model. The delta = 1 case, which previously did not converge, was found to not converge here either (and was due to exclusively the kappa matrix i.e. the constant term). Strategies between the two strategic agents appeared to decrease in each other, and a limit matrix was identified.
