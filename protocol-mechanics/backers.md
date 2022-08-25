# Backers

{% hint style="success" %}
**Backers optimize for yield and selection**

Backers are Investors who supply USDC to individual Borrower Pools. Backers evaluate individual deals, and lend directly to specific Borrower Pools with first-loss capital.&#x20;
{% endhint %}

## Supplying to Borrower Pools

Backers look at Borrower Pools as investment opportunities. They evaluate the information Borrowers provide, and decide if they want to supply first-loss capital (junior tranche) to fund a Borrower Pool.&#x20;

To track the different amounts that different participants supply, Backers receive an NFT when they supply capital. The NFT tracks the amount that was supplied and how much of it has been redeemed. At any time, a Backer can use their NFT to redeem their specific portion of the available repayments in the Pool.

The Senior Pool provides additional second-loss (senior tranche) capital to the Borrower Pool according to the [Leverage Model](leveragemodel.md). To account for the lower risk of the senior tranche, 20% of the senior tranche’s nominal interest is reallocated to the junior tranche. In addition, the protocol retains 10% of all interest payments as reserves, which are managed by the decentralized Governance.&#x20;

As a result, the Senior Pool earns an effective interest rate equal to 70% of the nominal interest rate. Or, in terms of the nominal interest rate, $$i_{n}$$ , protocol reserve allocation, $$p$$, and junior reallocation percent, $$j$$:

$$
i_{senior}=i_n*(1-p-j)
$$

Accordingly, based on these same inputs and the leverage ratio, $$r$$, Backers receive an effective interest rate of:

$$
i_{junior}=i_n*(1-p+r*j)
$$

**For example:** Consider a Borrower Pool with a 15% interest rate and 4.0X leverage ratio. If the Backers supply `$200K`, the Senior Pool will allocate another `$800K`. Assuming the Borrower borrows the full `$1M` for one year, they will pay `$1M * 15% = $150K` in interest. Of that, the Senior Pool receives `0.15*(1 - 0.1 - 0.2) = 10.5%` interest, or `$800K * 0.105 = $84K`. The Backers receive `0.15*(1 - 0.1 + 4*0.2) = 25.5%` interest, or `$200K * 0.255 = $51K`. The remaining `$15K` is the `10%` protocol reserve allocation.



For a step-by-step on supplying to Borrower Pools, read the documentation's [Investor How-To](../guides/) section.&#x20;

## Early Backer Rewards

It is easier to feel confident supplying to a Borrower Pool when a lot of other Backers have already vetted and supplied to it, and the Senior Pool is already adding leverage. It is riskier to be the first one in a Borrower Pool. To incentivize early Backers, the protocol provides an additional GFI reward to all Backers who contribute early on, with the reward amount decreasing for later Backers as the Borrower Pool reaches its limit.

The protocol assigns the reward when a Backer supplies, but the reward is not immediately claimable. The percent of the reward that is claimable is proportional to the percentage of the full expected repayment of principal plus interest that the Borrower successfully repays. This ensures the Backer only receives the early Backer reward after the Borrower Pool proves valuable to the protocol.

## Staking on Backers

{% hint style="info" %}
Note: As of August 2022 staking on Backers is not yet live on Goldfinch.&#x20;
{% endhint %}

In addition to evaluating individual Borrower Pools, Backers may also evaluate other Backers in order to give them leverage. Backers can do this by staking GFI directly on another Backer.

Based on the amount of GFI staked on a given Backer, the Senior Pool uses the Leverage Model to calculate a leverage ratio and allocate capital whenever that Backer supplies to Borrower Pools. For example, if a Backer has a leverage ratio of 4.0X based on the GFI staked on them by other Backers, then anytime they supply to a Borrower Pool, the Senior Pool will allocate 4.0X of that amount.

The Senior Pool provides this leverage up to a maximum total that is calculated as the leverage ratio multiplied by the total value of GFI staked on that Backer. For example, if the Backer has $1M worth of GFI staked on them with a 4.0X leverage ratio, the Senior Pool will allocate up to $4M total leverage.

When GFI is staked on a Backer, that GFI serves as collateral against potential defaults for that Backer’s positions in Borrower Pools. When a Borrower defaults, the GFI staked on all the Backers in that pool are reallocated to the senior tranche until the senior tranche is made whole on their expected payments. This incentivizes Backers to stake on other Backers who supply to safe Borrower Pools.

To reward Backers for staking GFI on other Backers, the protocol distributes GFI to them on a regular basis. The protocol allocates the distributions in proportion to the interest their leveraged GFI earns. This incentivizes Backers to stake on other Backers who supply to high-yielding Borrower Pools.

## Summary of Backer mechanics

Backers have an incentive to provide first-loss capital to Borrower Pools as they can receive both early Backer rewards and higher effective yields based on the Senior Pool leverage. In the future they will also have an incentive to stake GFI on other Backers as they will be able to earn additional rewards when that Backer supplies to Borrower Pools.&#x20;
