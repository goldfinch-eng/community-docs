# Senior Pool Liquidity Mining

Liquidity Providers can earn GFI by staking the FIDU they receive for supplying to the Senior Pool.

GFI tokens are granted at a variable distribution rate, which is based on a target pool balance set by Governance. More tokens are distributed when the pool is under the target, and less are distributed when it is over the target. The further under the target the pool balance is, the more GFI tokens are distributed. This helps incentivize a healthy utilization and APY for the pool, relative to loans outstanding.

All FIDU liquidity miners, including those who staked FIDU prior to the implementation of community proposal GIP-10 on July 20, 2022, can withdraw from staking at any time and receive the full value of their vested GFI liquidity mining rewards at withdrawal. See below for more details.



## Distribution rate

The GFI distributions rate is calculated using several parameters, all set by Governance:

* **Target balance:** The ideal total balance of the Senior Pool. The community can decide this balance based on expected future capital needs. It should be high enough to attract the amount of capital the protocol will need, but not too high that the protocol unnecessarily distributes GFI to unused capital.
* **Minimum rate:** The lowest possible rate of GFI distributed per second.
* **Maximum rate:** The highest possible rate of GFI distributed per second.
* **Target range:** T\he range around the "Target balance" along which the min and max distribution rate are applied. It is represented as two percentages (e.g. min: 50% of the target balance, max: 200% of the target balance).

The reward rate can be thought of as a piecewise linear function that looks something like this:

![](<../../.gitbook/assets/image (1).png>)

* Inside the target range, the distribution rate linearly decreases from "Maximum rate" to "Minimum rate"
* Below the target range, the distribution rate is constant at "Maximum rate"
* Above the target range, the distribution rate is constant at "Minimum rate"

In other words, when the pool balance is below its target, the distribution rate will be higher, incentivizing more people to supply capital to the pool. When the pool balance is above its target, the distribution rate will be lower, incentivizing withdrawals.

### Current parameters

As of January 11 2021, the distribution rate parameters have been set as follows:

* **Target balance:** $100M
* **Minimum rate:** 0 GFI
* **Maximum rate:** 0.5% of GFI supply per month (this equals 0.217438574961948 GFI / second)
* **Target range:** $50M to $200M (50% to 200%)

Governance can always decide to change these parameters.



## Unlock schedule

The GFI distributions received from liquidity mining can be withdrawn at any time, with no unlock period or slashing. FIDU stakers can stake and unstake at will without forfeiting any of the GFI rewards they have earned. You can learn how to stake FIDU in the Participating in Liquidity Mining section of the documentation.

**FIDU staked prior to July 20, 2022**

Before July 20, 2022, the GFI distributions received from liquidity mining unlocked linearly over the first 12 months of staking with early withdrawals forfeiting any remaining locked rewards. This meant that a liquidity provider could withdraw from staking whenever they chose, but would forfeit some GFI distributions if they withdrew before 12 months.

This was updated by the implementation of community proposal GIP-10 to make the GFI rewards received for liquidity mining withdrawable at any time with no unlock period or slashing. To ensure that the new system did not hurt existing FIDU stakers in any way when implemented, the proposal also removes slashing for Liquidity Providers who staked FIDU before July 20, 2022.

If a Liquidity Provider who staked FIDU before July 20, 2022 withdraws, the part of their GFI rewards that would have been slashed under the original rewards design will instead not be slashed and will unlock over their remaining 12 month period. The Liquidity Provider will continue to earn their remaining GFI rewards, and can un-stake and re-stake their FIDU to begin receiving GFI rewards with no unlock/vesting period moving forward.

