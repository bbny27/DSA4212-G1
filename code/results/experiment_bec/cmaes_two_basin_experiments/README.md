# CMA-ES on a two-basin objective

We investigated when CMA-ES discovers a better basin and when it
converts that discovery into a precise solution under a fixed budget.

## How to read the results

- Discovery means at least one evaluated point had f < 1.
- Precision means at least one evaluated point had f < 0.01.
- Finishing near B means the final sampling distribution was centred
  and concentrated near B according to the experiment's D_b cutoff.

## Experiments and findings

1. Population and parent count. The factorial comparison varied
   lambda and mu separately. Doubling lambda improved discovery
   and final concentration near B in the tested comparisons with
   mu fixed. Increasing mu had a more mixed effect.

2. Convergence sweeps. With mu = lambda/2, larger populations
   generally improved discovery under 200 evaluations. Very large
   populations often refined less successfully. For c = 30 and
   starts near B, lambda 16 to 48 increased discovery from 46/60
   to 59/60, while precision fell from 22/60 to 12/60.

3. Wide domain. With the box widened to [-20, 20]^2 and the minima
   farther apart, discovery from near A became rare, especially
   at c = 30. The box, separation, starting offsets and physical
   initial spread changed together.

4. Initial spread. In the wide domain with starts close to B,
   physical initial SD 2.4 reached f < 0.01 in 60/60 runs at
   c = 30, versus 0/60 with SD 12. From near A, both spreads
   rarely found B.

5. Intermediate domain. The [-10, 10]^2 sweep repeats the
   population and parent-count comparisons at intermediate basin
   separation. See the exported summary and plots for its results.

6. Update rules. At fixed lambda = 12 and mu = 6, holding the
   step size fixed improved discovery from near A at c = 30
   (30/60 versus 13/60), with little gain in precision
   (6/60 versus 5/60). Halving the mean update improved precision
   from near B at c = 30 (33/60 versus 16/60).

## Scope

These results describe the tested landscape, starts and evaluation
budgets. The settings that helped discovery and those that helped
refinement depended on the starting location and landscape.
