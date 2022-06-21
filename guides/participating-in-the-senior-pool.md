---
description: This section covers instructions on supplying / staking in the Senior Pool
---

# Participating in the Senior Pool

[Liquidity Providers](../protocol-mechanics/liquidityproviders.md) participate in the the Senior Pool to earn passive yield. The Senior Pool is a smart contract that automatically allocates capital across all Borrower Pools according to the consensus those pools receive from Backers.&#x20;

## Learning about the Senior Pool

#### How the Senior Pool works

Read about the Senior Pool on the [Liquidity Providers page](../protocol-mechanics/liquidityproviders.md).

#### Understanding the risks

<mark style="color:red;">**It is important to understand that you can lose money by participating in the Senior Pool.**</mark>** ** If a Borrower never pays back the amount they borrow, you will lose your relative portion of that loan default. However, if a Borrower pays back a portion of what they owe, that payment will go to the Senior Pool first, before it starts to cover any losses for Backers. In this way the Senior Pool providers more protection, compared to participating directly in Borrower Pools as a Backer.

#### Understanding the APY

The APY shared at the top of the [Senior Pool page](https://app.goldfinch.finance/pools/senior) is based on a current snapshot in time, and changes depending on two factors.&#x20;

1. The first factor is the amount of money in the Senior Pool. All interest payments from Borrower Pools is automatically allocated across the money in the Senior Pool. So as more capital is supplied to the senior pool, the effective yield will decline because the payments are spread across more capital.
2. The second factor is how much capital has been deployed across Borrower Pools. As more capital is deployed, increasing utilization, that means there will be more payments, thereby increasing APY.&#x20;

The APY described is therefore a dynamic number that will change both as Liquidity Providers supply/withdraw from the pool, and as Borrowers make drawdowns and repayment.

## Supplying to the Senior Pool

1. Go to [https://app.goldfinch.finance/pools/senior](https://app.goldfinch.finance/pools/senior).
2. Ensure your wallet is connected by clicking `Connect`.
3. Ensure you have [verified your identity](verifying-your-identity.md).
4. Click `Supply` and enter the amount of USDC you would like to supply to the Senior Pool.
5. Ensure you check off `I agree to the` [`Senior Pool Agreement`.](https://murmuration.goldfinch.finance/senior-pool-agreement-non-us)
6. If you check off `I want to stake my supply to earn GFI rewards (some additional APY)`, you will receive additional GFI distributions.&#x20;
   * Please note: Staking does not 'lock' your USDC; you can always withdraw at any time. Staking allows you to receive GFI distributions, which unlock over the first 12 months after staking. For more details, see [Senior Pool Liquidity Mining](../protocol-mechanics/investor-incentives/senior-pool-liquidity-mining.md).
   * You can see your GFI for staking FIDU in the `GFI` tab.
7. Click `Submit`.
8. Accept the transaction on your wallet.
9. Done. You should now see the additional USDC in your balance at the top of the page.

## Withdrawing from the Senior Pool

{% hint style="info" %}
Note: There is a 0.5% fee when withdrawing from the Senior Pool
{% endhint %}

1. Go to [https://app.goldfinch.finance/pools/senior](https://app.goldfinch.finance/pools/senior).
2. Click `Withdraw` and enter the amount of USDC you want to withdraw
   1. Please note: If you previously staked your FIDU, withdrawing will also unstake your FIDU.
   2. You will receive this amount minus a 0.5% fee that goes towards protocol reserves. The dapp will state what amount you will get right below the amount you stated.
3. Click `Submit.`
4. `Accept` the transaction on MetaMask.
5. Done. You should now see the additional USDC in your wallet.

## Viewing your FIDU in Metamask

1. FIDU should appear in the assets tab on Metamask
2. If it doesn't appear, click import token at the bottom of the assets tab, then custom token. Input the FIDU token address, which is `0x6a445e9f40e0b97c92d0b8a3366cef1d67f700bf`, and click Add Custom Token. It should now appear in your assets list.

## FAQ

#### **Can I withdraw immediately from the Senior Pool?**

Yes, as long as there is enough USDC remaining in the Senior Pool. If the Senior Pool is 100% utilized and there is no USDC remaining, you will need to wait for other Liquidity Providers to supply first, or for Borrowers to make repayments.

#### **What cryptoassets can I supply to the Senior Pool?**

The Senior Pool only supports USDC.

#### **When do I receive yield?**

You receive yield each time Borrowers make interest payments into their Borrower Pools. Borrowers are typically on monthly payment schedules, and different Borrowers make their payments at different times in the month.

#### What is FIDU?

FIDU is like a "digital receipt" that represents how much you have supplied to the pool It is very similar to [Compound's cTokens](https://compound.finance/docs/ctokens). For more information, see [FIDU in Liquidity Providers](../protocol-mechanics/liquidityproviders.md).



