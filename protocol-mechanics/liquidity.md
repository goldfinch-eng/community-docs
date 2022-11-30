# Liquidity & LP Withdrawals

## Senior Pool LPs: FIDU Liquidity via Withdrawal Requests

* As outlined in [GIP-25](https://gov.goldfinch.finance/t/gip-25-senior-pool-periodic-withdrawal-requests/1183/7), LPs must now submit a Withdrawal Request to withdraw FIDU from the Senior Pool. There is a 0.5% withdrawal fee for redeeming FIDU for USDC.&#x20;
* A single Withdrawal Request may be fulfilled over multiple distribution periods.
* Distributions happen every 2 weeks, and distribution amounts are variable based on availability of capital in the Senior Pool and total amount requested.
* A Withdrawal Request remains active until it is completely fulfilled or canceled. Once a Withdrawal Request has been made, it can only be increased or canceled, not reduced.&#x20;
* If a Request is canceled before it is fully fulfilled, the LP is charged a cancellation fee of 1% of the total request.

At any time, Senior Pool[ Liquidity Providers](https://docs.goldfinch.finance/goldfinch/protocol-mechanics/liquidityproviders) with a[ Unique Identity NFT (UID)](https://docs.goldfinch.finance/goldfinch/unique-identity-uid) may submit a request to withdraw USDC from the Senior Pool by depositing their FIDU into a Withdrawal Request. .There is a 0.5% withdrawal fee for redeeming FIDU for USDC on Goldfinch, contributing funding to the Goldfinch treasury.&#x20;

FIDU that is staked or supplied to a Membership Vault must be unstaked or removed from the Vault before an LP can submit a request to withdraw it from the Senior Pool.&#x20;

Various Goldfinch community members and third-parties have taken steps to create additional mechanisms to withdraw capital from the Senior Pool when there is no excess USDC due to high utilization rates. For example, two community members created a withdrawal mechanism via a[ FIDU-USDC Curve pool](https://medium.com/@alvinhsia/increasing-access-and-interoperability-on-goldfinch-finance-e62e4f3682e4).\*

### **Withdrawal Distributions**

Withdrawal Requests are fulfilled every two weeks. If there is enough USDC unutilized in the Pool to honor all outstanding withdrawal requests at the end of the distribution period, all withdrawers will receive 100% of the value of the FIDU they requested to withdraw, in USDC.

If there is not enough USDC in the Senior Pool to honor all outstanding Withdrawal Requests at the end of the period, due to the USDC being actively utilized by Borrowers, all available USDC will be allocated to withdrawers pro-rata.

For example, if there is enough USDC in the Senior Pool at the end of the period to fulfill 80% of the current Withdrawal Requests, all withdrawers will receive 80% of the value of the FIDU they’ve requested to withdraw.

Withdraw Requests that are partially filled will be automatically rolled over into the next period, and one’s Withdrawal Request remains active until it is completely fulfilled or canceled. An LP can only have one active Request at a time, although they can increase that request while it is active.

Once a Withdrawal Request has been made, it can only be increased or canceled, not reduced. If a Request is canceled before it is fully fulfilled, the LP is charged a cancellation fee of 1% of the total remaining request.

### Withdrawal Request FAQs&#x20;

**Will I be able to participate in staking rewards while my FIDU is in the Withdrawal Request?**&#x20;

No, staked FIDU must be unstaked before it can be deposited to a Withdrawal Request.

Any staked FIDU that is supplied to a Membership Vault must be withdrawn from the Membership Vault before it can be un-staked. Then, it must be un-staked before it can be deposited to a Withdrawal Request.

As such, neither staking rewards nor Member Rewards can be earned while FIDU is in the Withdrawal Request.

**Will I earn interest from the Senior Pool while I’m withdrawing?**&#x20;

Yes, FIDU that is in an active Withdrawal Request, including both new Requests and rollover Request balances, will continue to appreciate in value while it is pending withdrawal. LPs will still benefit from interest payments that the Senior Pool receives.

However, USDC that has been distributed to an LP at the end of a withdrawal period, but that the LP has not yet withdrawn from the dapp, will not accrue any further interest.

**Why not a queue?**&#x20;

In a withdraw queue system, if a large FIDU holder submitted a large withdraw request they could reserve 100% of the incoming capital to the Senior Pool until their request was completely filled. This would prevent other FIDU holders from withdrawing any amount of their position.

**How will this solution affect bots?**&#x20;

Speed of withdrawal will no longer be an advantage for withdrawing capital from the Senior Pool. Bots will need to submit a Withdrawal Request to withdraw, like any other LP.

## Backer Position: PoolToken NFT

[Backers ](backers.md)with a [Unique Identity NFT (UID)](../unique-identity-uid/) may withdraw interest payments as they are paid by the Borrower, which is monthly across all Goldfinch Borrower Pools as of August 2022. Principal liquidity is dependent on the Pool term as proposed by the Borrower, currently three years on average as of August 2022.

There is no withdrawal fee for claiming a Backer’s share of a Pool’s interest repayments or principal.

The Goldfinch dapp does not directly support PoolToken NFT secondary sales. However, community members and third-parties have launched various integrations via governance to provide Backers with the ability to sell their PoolToken NFTs. For example, [AlloyX launched a Goldfinch integration](https://medium.com/goldfinch-fi/lockup-free-goldfinch-investment-is-here-powered-by-alloyx-b683c48becb4), and the Goldfinch community is launching a [community-driven PoolToken NFT market](https://gov.goldfinch.finance/t/gip-15-secondary-marketplace-for-borrower-pool-positions/1044) that will allow backers to sell their PoolToken NFTs.\*

_\*Please note that neither the FIDU-USDC Curve Pool, PoolToken NFT market, integrations, nor any other marketplace outside the Goldfinch dapp, are built and maintained by Goldfinch. Therefore, you should use your own judgment before selling FIDU or Backer PoolToken NFTs outside of the Goldfinch dapp._
