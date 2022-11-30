# Liquidity Providers

{% hint style="success" %}
**Liquidity Providers optimize for diversification and liquidity**&#x20;

Liquidity Providers are Investors who supply USDC to Goldfinch by investing in the Senior Pool. This Senior Pool capital is automatically allocated across Borrower Pools.
{% endhint %}

## Supplying to the Senior Pool

Liquidity Providers supply capital to the Senior Pool in order to earn yields optimized for ease and diversification. The Senior Pool automatically allocates that capital across the senior tranches (second-loss) of Borrower Pools according to the [Leverage Model](leveragemodel.md).&#x20;

In this way, when more Backers actively evaluate a Pool's terms and decide to invest first-loss capital in it, the Senior Pool will in turn automatically allocate more second-loss capital to the Pool. The Senior Pool thereby provides both diversification across Borrower Pools and seniority to the first-loss capital of Backers. This process does not involve seeking the permission of different Borrowers.

To compensate Backers for providing the work of both evaluating Borrowers Pools and providing first-loss capital, 20% of the Senior Pool’s nominal interest is reallocated to Backers.

As a result, the Senior Pool earns an effective interest rate equal to 70% of the nominal interest rate. Or, in terms of the nominal interest rate, $$i_{n}$$, protocol reserve allocation, $$p$$​, and junior reallocation percent, $$j$$:&#x20;

$$
i_{senior}=i_n*(1-p-j)
$$

Accordingly, based on these same inputs and the leverage ratio, $$r$$​, Backers receive an effective interest rate of:&#x20;

$$
i_{junior}=i_n*(1-p+r*j)
$$

​**For example:** Consider a Borrower Pool with a 15% interest rate and 4.0X leverage ratio. If the Backers supply `$200K`, the Senior Pool will allocate another `$800K`. Assuming the Borrower borrows the full `$1M` for one year, they will pay `$1M * 15% = $150K` in interest. Of that, the Senior Pool receives `0.15*(1 - 0.1 - 0.2) = 10.5%` interest, or `$800K * 0.105 = $84K`. The Backers receive `0.15*(1 - 0.1 + 4*0.2) = 25.5%` interest, or `$200K * 0.255 = $51K`. The remaining `$15K` is the `10%` protocol reserve allocation.



For a step-by-step on supplying to the Senior Pool, read the documentation's [Investor How-To](../guides/) section.

## FIDU <a href="#fidu" id="fidu"></a>

When Liquidity Providers supply to the Senior Pool, they receive an equivalent amount of FIDU. FIDU is an ERC20 token.

At any time, Liquidity Providers can withdraw their position by depositing their FIDU to a [Withdrawal Request](https://docs.goldfinch.finance/goldfinch/protocol-mechanics/liquidity), to redeem their FIDU for USDC at an exchange rate based on the net asset value of the Senior Pool, minus a 0.5% withdrawal fee. This exchange rate for FIDU increases over time as interest payments are made back to the Senior Pool.

Withdrawal Requests are fulfilled every two weeks. It is possible that when a Liquidity Provider wants to withdraw, the Senior Pool may not have sufficient USDC because it has been borrowed by Borrowers. If there is enough USDC unutilized in the Pool to honor all outstanding withdrawal requests at the end of the distribution period, all withdrawers will receive 100% of the value of the FIDU they requested to withdraw, in USDC, minus the 0.5% withdraw fee.

If there is not enough USDC in the Senior Pool to honor all outstanding Withdrawal Requests at the end of the period, due to the USDC being actively utilized by Borrowers, all available USDC will be allocated to withdrawers pro-rata

You can learn more about how Withdrawal Requests work in the [Liquidity section](https://docs.goldfinch.finance/goldfinch/protocol-mechanics/liquidity) of the documentation.

## Summary of Liquidity Provider mechanics

Liquidity providers are incentivized to supply to the Senior Pool in order to earn automatically allocated yields, as their capital is diversified across different Borrower Pools.&#x20;
