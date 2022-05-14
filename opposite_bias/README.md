# Opposite Bias Models

This folder contains notebooks regarding models where strategic agents have agendas biased in opposite directions.

## October 2021

### [Quick Test](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/opposite_bias/quick_test.pdf)
This notebook is a quick test of the model with strategic agents with opposing agendas and explores several cases and comparative statics.
```
In the examples with the 10 and -5 agent agendas, the steady-state opinion is 0.609 (closer to the -5).
In the perfect opposite case (10 and -10), it is exactly in between: 0.
In the deviating from perfect opposite case (10 and just slightly above -10), it is a very small positive number (but still closer to the slightly above -10 agenda).
In the greater deviation case (10 and -9), the opinion is 0.122 (the midpoint is 0.5 so since 0.122 < 0.5, it is closer to the -9).
If I then create a new case with 5 and -9 (shifting the 10), the opinion is -0.487 (the midpoint is -2 so now this is closer to the 5).
The steady-state opinion does not seem to depend on the starting opinion either.
It also appears to depend on the R matrix and the r cost normalization variable. If I lower R in the 10 and -5 case from 1 to 0.2, the steady-state opinion becomes 1.495 (higher). As R goes to zero, the opinion goes to the midpoint of 10 and -5 (2.5).
This then implies that cost is the factor that causes the "opinion bias" in the model, and thus why changing the r normalization would affect the opinion as well.
```

## November 2021

### [Addendum](https://github.com/jbrightuniverse/strategic_influencer_of_naive_agents/blob/main/opposite_bias/addendum.pdf)
This notebook checks an additional case concerning why r^1 and r^2 do not appear inversely related.
