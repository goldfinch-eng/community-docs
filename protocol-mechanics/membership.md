---
description: >-
  Join a Membership Vault as an active Goldfinch Investor to upgrade your
  Goldfinch participation and support Goldfinch’s growth and expansion.
---

# Membership

## Introduction to Goldfinch Membership

* Goldfinch Membership is the first phase of a broader tokenomics redesign ([Tokenomics v2](https://gov.goldfinch.finance/t/grc-01-goldfinch-v2-tokenomics-outline/995)), which was approved by the community in 2022 and focuses on enhancing the utility of GFI.&#x20;
* Membership is designed to empower Goldfinch Investors to support the protocol’s growth while increasing their participation.

Goldfinch Members receive yield enhancements via Member Rewards, which have been earmarked from the Goldfinch treasury and are distributed pro-rata based on one’s Membership Vault position. In addition, Members will gain access to exclusive communication channels, special offers, and more.

Encouraging Investors to hold GFI will help to increase community participation in [governance](https://docs.goldfinch.finance/goldfinch/governance)—which requires GFI—as well as further aligning and incentivizing the Goldfinch community’s interest in the long-term success of the protocol.

Membership also encourages the single biggest lever for network growth, increased TVL, resulting in a more robust and secure protocol ecosystem while also rewarding the global community of Goldfinch participants who continue to contribute to Goldfinch’s growth and resilience.&#x20;

## Becoming a Goldfinch Member&#x20;

* There are only two requirements to participate in Goldfinch Membership: being a [Senior Pool LP](liquidityproviders.md) or [Backer](backers.md) on Goldfinch (represented by holding staked FIDU and/or an active Backer NFT), and holding [GFI](gfi-token.md).
* To become a Member, one only needs to lock their staked FIDU or Backer NFTs, plus GFI, into the [Membership Vault in the Goldfinch dapp](https://app.goldfinch.finance/membership).&#x20;
* To optimize the yields you can receive, balanced is best: matching the dollar value of the GFI and assets you deposit to the vault will balance the vault ratio and increase your potential Member Reward yield.

You can withdraw your deposited assets from the vault at any time, and there is no risk of slashing when participating in a Membership Vault. However, if you withdraw your assets from the vault before the end of a reward cycle (weekly), you will forfeit any Member Rewards accumulated during that cycle.

While future releases are expected to launch support for joining a Membership Vault by depositing Curve FIDU/USDC LP Tokens or staked Curve FIDU/USDC LP Tokens, at launch the vaults only accept Backer PoolToken NFTs, representing participation in a Goldfinch Borrower Pool, or staked FIDU, Goldfinch Senior Pool tokens that have been staked in the dapp to receive extra GFI rewards. If you hold unstaked FIDU, you can stake it to be able to supply it to a Membership Vault by following [this guide](../guides/participating-in-liquidity-mining.md).

## Member Rewards&#x20;

* Member Rewards are a form of yield enhancement to further align and incentivize Goldfinch Investors’ interest in the long-term success of the protocol.&#x20;
* Member Rewards are distributed weekly in [FIDU](liquidityproviders.md#fidu).

Member Rewards come from an earmarked percentage of Goldfinch’s Treasury, and are paid pro-rata to Members—meaning that the higher the percentage of the Membership Vault’s assets one supplied during a reward cycle, the higher percentage of Member Rewards one will receive for that cycle.

Member Rewards are distributed weekly in FIDU, naturally increasing Members’ exposure to Goldfinch’s Senior Pool to increase their opportunities to receive yields. Rewards must be claimed manually, can then be staked to receive additional GFI rewards, and then can be deposited to the Membership Vault alongside GFI, increasing one’s interest in the Membership Vault to receive additional Member Rewards.

If a participant deposits assets into the Membership Vault during a weekly reward cycle their assets will begin accumulating Member Rewards at the beginning of the next weekly reward cycle. While Members can withdraw their deposited assets at any time to exit Membership, if they withdraw before the end of a weekly reward cycle they will forfeit any Member Rewards they would have received during that cycle.

Following launch, Members will also have access to exclusive communication channels, special offers, and more.

### Member Rewards calculation

The Member Rewards share calculation is a governance-controlled parameter that determines the optimal share of Capital and GFI for maximizing rewards in Membership Vaults.

\
A Member’s precise share of Member Rewards is calculated using the [Cobb-Douglas function](https://en.wikipedia.org/wiki/Cobb%E2%80%93Douglas\_production\_function), an equation commonly used in economic analysis for balanced input relationships generating an output, and also used by protocols such as 0x and The Graph for reward systems. \
\
All values are for a given weekly period:

<figure><img src="https://global.discourse-cdn.com/standard17/uploads/goldfinch/optimized/1X/db6299b2c7a1f16e91500690ed425badbf42e3ea_2_517x274.png" alt=""><figcaption></figcaption></figure>

The two variables in the Member Reward equation that are determined by governance are:

* μ = Share of earmarked treasury used for Member Rewards
  * You can think of this as “What percentage of the earmarked treasury allocation should be allocated to members?”
  * Currently, μ = 50%
* α = Capital supply amplification weight.
  * You can think of this as “How much should we weight locked capital supply, versus locked GFI for fee shares?”
  * Currently α = 0.50

The μ and α values can be changed by governance vote. μ = 50% allows the protocol to build sufficient stablecoin reserves for future needs, like community grants, and α = 0.50 is a good starting point to observe how dynamics play out between the balances of capital supply and GFI.\
\
You can learn in-depth about how Member Rewards are calculated in the original [Membership Governance proposal (GIP-13)](https://gov.goldfinch.finance/t/gip-13-tokenomics-update-phase-1-membership-vaults/996#member-reward-share-calculation-9).

### How are the estimated Member Rewards in the app calculated?&#x20;

The estimated Member Rewards displayed in the Goldfinch platform are calculated based on a) one’s Membership Vault position, and b) on the distribution of total capital in the Membership Vault overall.&#x20;

* This number is an estimate because rewards are distributed pro-rata to Members at the end of each reward cycle—as such, oter Investors entering or exiting the Membership Vault during a reward cycle will change the percentage of rewards one is expected to receive, due to changing what percentage of the Vault one’s individual position represents.\

* The estimated Member Rewards displayed is a dynamic number that reflects the distribution of total capital in the Membership Vault overall at that moment in time and one’s Member Vault position at that moment in time.
