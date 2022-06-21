# Senior Pool Liquidity Mining

Participants can earn GFI by staking the FIDU they receive from supplying to the Senior Pool.

GFI tokens are granted at a variable distribution rate, which is based on a target pool balance set by Governance. More tokens are distributed when the pool is under the target, and less are distributed when it is over the target. The farther under the target the pool balance is, the more GFI tokens are distributed. This helps incentivize a healthy utilization and APY for the pool, relative to loans outstanding.

Also, to encourage long-term participation, the GFI distributions received from liquidity mining unlock linearly over the first 12 months of staking. This means that while you can withdraw whenever you like, if you withdraw before 12 months, you will forfeit some of your GFI distributions. For example, after 3 months you'd forfeit 75%, after 6 months you'd forfeit 50%, and so on. After 12 months, you will continue to receive distributions, and will never forfeit any GFI. See below for more details.



## Distribution Rate

The GFI distributions rate is calculated using several parameters, all set by Governance:

* **Target balance**. This is the ideal total balance of the Senior Pool. The community can decide on this balance based on expected future capital needs. It should be high enough to attract the amount of capital the protocol will need, but not too high that the protocol unnecessarily distributes GFI to unused capital.
* **Minimum rate:** This is the lowest possible rate of GFI distributed per second.
* **Maximum rate:** The is the highest possible rate of GFI distributed per second.
* **Target range:** This is the range around the "Target balance" along which the min and max distribution rate are applied. It is represented as two percentages (e.g. min: 50% of the target balance, max: 200% of the target balance).

The reward rate can be thought of as a piecewise linear function that looks something like this:

![](<../../.gitbook/assets/image (1).png>)

* Inside the target range, the distribution rate linearly decreases from "Maximum rate" to "Minimum rate"
* Below the target range, the distribution rate is constant at "Maximum rate"
* Above the target range, the distribution rate is constant at "Minimum rate"

In other words, when the pool balance is below its target, the distribution rate will be higher, incentivizing more people to supply capital to the pool. When the pool balance is above its target, the distribution rate will be lower, incentivizing withdrawals.

### Current Parameters

As of January 11 2021, the distribution rate parameters have been set as follows:

* **Target balance:** $100M
* **Minimum rate:** 0 GFI
* **Maximum rate:** 0.5% of GFI supply per month (this equals 0.217438574961948 GFI / second)
* **Target range:** $50M to $200M (50% to 200%)

Governance can always decide to change these parameters.



## Unlock Schedule

To encourage long-term participation, the GFI distributions received from liquidity mining unlock linearly over the first 12 months of staking. This means that while you can withdraw whenever you like, if you withdraw before 12 months, you will forfeit some of your GFI distributions. For example, after 3 months you'd forfeit 75%, after 6 months you'd forfeit 50%, and so on. After 12 months, you will continue to receive distributions, and will never forfeit any GFI. See below for more details.

#### **Withdrawals**

Withdrawing from the Senior Pool will cause still-locked GFI distributions to be forfeited, proportional to the size of withdrawal. The amount that’s forfeited is purely linear. If you are 1/4 through the year, you’ll forfeit 3/4 of your potential rewards. If you’re 3/4 way through, you’ll forfeit 1/4 of your rewards. See the example below. Already unlocked GFI is untouched and claimable at any time, even after withdrawing funds from the Senior Pool.

If you have supplied multiple times in the Senior Pool and wish to withdraw, the unlock schedules are exited from most recent end time to least recent end time — in other words, unlock schedules that have not been completed will be exited before unlock schedules that have been completed. This approach maximizes the rate at which you continue to receive the earliest-claimable distributions.

#### **Example**

Let's say that you supplied 10,000 USDC on Feb 1. Then 9 months later, on Nov 1, you go to withdraw all of it. Let’s say you’ve received 1,000 GFI from liquidity mining by that point. On that date, you would receive 750 GFI that is unlocked and claimable, but you would forfeit the remaining 250 GFI (25% of those distributions).

If instead you waited the full year, then perhaps by then you would have earned 1,250 GFI. By withdrawing on that date a full year later, you would forfeit no GFI and receive the full 1,250.

