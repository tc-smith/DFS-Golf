# DFS-Golf
Here are several notebooks solving the 0/1 knapsack problem for fantasy golf lineups.

The notebooks here solve the n-dimensional 0-1 knapsack problem of roster selection for DFS golf.  A roster of 6 players with a maximum cumulative salary of $50000 is allowed.  This notebook uses Establish The Run's DK Points projections to find the optimal roster based on points projection.  The projections are available for download through ETR's golf subscription.

The following is the constraint problem setup:

maximize $$\sum_{i=1}^n v_i x_i$$

subject to 

$$\sum_{i=1}^n w_i x_i <= 50000$$

$$\sum_{i=1}^n x_i == 6$$

$$x_i \in \{0, 1\}$$

Here, $x_i$ is a 0-1 variable representing whether player i is included in the roster.  $v_i$ represents ETR's points projection for player i.  $w_i$ represents the DK salary for player i.

The notebooks differ in what solver is used.  The mip linear solver notebook includes code to generate multiple lineups by varying the player projections according to player volatility.
