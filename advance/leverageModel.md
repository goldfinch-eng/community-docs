# Leverage Model
---

?> The Leverage Model determines how much capital the Senior Pool allocates toward
each Borrower Pool, based on how much it `trusts` each Borrower Pool.

## Trust Through Consensus
In order to determine how to allocate capital from the Senior Pool, the protocol uses a
principle of "trust through consensus." This means that while the protocol doesn't trust
any individual Backer or Auditor, it does trust the collective actions of many of them. At
a high level: when more Backers supply to a given Borrower Pool, the Senior Pool
increases the ratio with which it adds leverage.

Because this approach relies on counting individual Backers, the protocol must ensure
they are in fact represented by different people. Therefore, all Backers, Borrowers, and
Auditors require a `unique entity check` to participate (see the [Unique Entity Check
section](/advance/uniqueEntityCheck.md)).

## Leverage Model Formula
The leverage amount, A, that the Senior Pool allocates is determined by the formula, where:

-  S is the total capital supplied by Backers.
-  D is the distribution adjustment on a scale of 0 to 1, which accounts for how
evenly distributed the Backers are. D is closer to 0 when the distribution is
skewed and closer to 1 when the Backers are more equally distributed. This
ensures no single Backer has an outsized influence. The formula for D uses the
percent supplied by each Backer, s<sub>n</sub>
, and is based on the Herfindahl-Hirschman Index: 
>![sigma](https://latex.codecogs.com/svg.latex?D%20=%201-\sum_{i=1}^n%20s_n^2)

- L is the leverage ratio on a scale of 0 to the maximum potential leverage ratio.
  Based on the number of Backers, b, the leverage ratio increases linearly from
  B<sub>min</sub>
  , the minimum number of Backers necessary for leverage, to B<sub>max</sub>
  , the
  maximum number of Backers necessary to achieve the maximum potential
  leverage, L<sub>max</sub>:
  
  >![sigma](https://latex.codecogs.com/svg.latex?L=L_{max}*\frac{max(0,%20b-B_{min})}{B_{max}-B_{min}})
