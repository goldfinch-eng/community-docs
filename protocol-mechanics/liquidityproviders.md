# Liquidity Providers

{% hint style="success" %}
Liquidity Providers are Investors who supply capital to Goldfinch by investing in the Senior Pool. This Senior Pool capital is automatically allocated across Borrower Pools via the Pools' senior tranches (second-loss) according to the Leverage Model.
{% endhint %}

## Supplying to the Senior Pool

Liquidity Providers supply capital to the Senior Pool in order to earn yields optimized for ease and diversification. The Senior Pool automatically allocates that capital across the senior tranches (second-loss) of Borrower Pools according to the [Leverage Model](leveragemodel.md). The Senior Pool thereby provides both diversification across Borrower Pools and seniority to the first-loss capital of Backers. This process does not involve seeking the permission of different Borrowers.

To compensate Backers for providing the work of both evaluating Borrowers Pools and providing first-loss capital, 20% of the Senior Pool’s nominal interest is reallocated to Backers.

For a step-by-step on supplying to the Senior Pool, read the documentation's [Investor How-To](../guides/) section.

## FIDU <a href="#fidu" id="fidu"></a>

When Liquidity Providers supply to the Senior Pool, they receive an equivalent amount of FIDU. FIDU is an ERC20 token. At any time, Liquidity Providers can withdraw their position by redeeming their FIDU for USDC at an exchange rate based on the net asset value of the Senior Pool, minus a 0.5% withdrawal fee. This exchange rate for FIDU increases over time as interest payments are made back to the Senior Pool.

It is possible that when a Liquidity Provider wants to withdraw, the Senior Pool may not have sufficient USDC because it has been borrowed by Borrowers. In this event, the Liquidity Provider may return when new capital enters the Senior Pool through Borrower repayments or new Liquidity Providers.

## Summary of Liquidity Provider mechanics

Liquidity providers are incentivized to supply to the Senior Pool in order to earn automatically allocated yields, as their capital is diversified across different Borrower Pools.&#x20;
