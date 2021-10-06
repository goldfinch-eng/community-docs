# Liquidity Providers


{% hint style="success" %}
Liquidity Providers supply capital to the Senior Pool in order to earn passive yield. The Senior Pool automatically allocates their capital to the senior tranches of Borrower Pools.
{% endhint %}


## Supplying to the Senior Pool

Liquidity Providers supply capital to the Senior Pool in order to earn passive yield. The Senior Pool then automatically allocates that capital across the senior tranches of Borrower Pools according to the Leverage Model. The Senior Pool thereby provides both diversification across Borrower Pools and seniority to the first-loss capital of Backers. Supplying capital to the Senior Pool is also fully permissionless.

To compensate Backers for both evaluating Borrowers Pools and providing first-loss capital, 20% of the Senior Pool’s nominal interest is reallocated to Backers.

## FIDU

When Liquidity Providers supply to the Senior Pool, they receive an equivalent amount of FIDU. FIDU is an ERC20 token. At any time, Liquidity Providers can withdraw by redeeming their FIDU for USDC at an exchange rate based on the net asset value of the Senior Pool, minus a 0.5% withdrawal fee. This exchange rate for FIDU increases over time as interest payments are made back to the Senior Pool.

It is possible that when a Liquidity Provider wants to withdraw, the Senior Pool may not have sufficient USDC because it has been borrowed by Borrowers. In this event, the Liquidity Provider may return when new capital enters the Senior Pool through Borrower repayments or new Liquidity Providers.

## Summary of Investor Incentives

Investors are incentivized to supply to the Senior Pool in order to earn passive yield.

