# Staking

There are currently two types of staking accessible on the Goldfinch protocol. All staking and participation incentives are driven and established via Goldfinch’s community governance process. Staking can be accessed in the Goldfinch protocol application at [app.goldfinch.finance/stake](https://app.goldfinch.finance/stake).

### Staking FIDU-USDC Curve LP Positions

Following a successful [community governance proposal](https://gov.goldfinch.finance/t/gip-01-allow-fidu-usdc-curve-lp-positions-to-be-staked-for-gfi-liquidity-mining-rewards/734), Liquidity Provider (LP) positions from participation in the Curve FIDU-USDC Pool can be staked on Goldfinch to receive additional GFI liquidity mining rewards.

GFI rewards for staking Curve LP positions come from the existing distribution parameters of the Senior Pool Liquidity Mining program, including being subject to the same unlock schedule as well.

#### Current Parameters

As of January 11 2021, the distribution rate parameters have been set as follows:

* **Target balance:** $100M
* **Minimum rate:** 0 GFI
* **Maximum rate:** 0.5% of GFI supply per month (this equals 0.217438574961948 GFI / second)
* **Target range:** $50M to $200M (50% to 200%)

Governance can always decide to change these parameters.

#### Unlock Schedule

To encourage long-term participation, the GFI distributions received from liquidity mining unlock linearly over the first 12 months of staking. This means that while you can withdraw whenever you like, if you withdraw before 12 months, you will forfeit some of your GFI distributions. For example, after 3 months you'd forfeit 75%, after 6 months you'd forfeit 50%, and so on. After 12 months, you will continue to receive distributions, and will never forfeit any GFI. See below for more details.

You can read Goldfinch’s documentation on Senior Pool Liquidity Mining to learn more about the Senior Pool Liquidity Mining’s GFI distribution rate, parameters, and unlock schedule, which are the same parameters used for Staking FIDU-USDC Curve LP Positions.

Participants can deposit their unstaked FIDU or USDC into the Curve FIDU-USDC liquidity pool by visiting the [Stake](https://app.goldfinch.finance/stake) tab on the Goldfinch protocol platform, and selecting either Deposit FIDU or Deposit USDC under LP on Curve. In the same interface, a participant can select the check box to simultaneously stake their resulting Curve LP positions on the Goldfinch platform in order to receive GFI rewards for their participation.

In addition, those participating in Senior Pool Liquidity Mining by staking FIDU on Goldfinch can also deposit their staked FIDU into the Curve FIDU-USDC liquidity pool via the Goldfinch protocol platform, to earn additional LP rewards without needing to unstake from Goldfinch. Participants can migrate their staked FIDU to deposit into the Curve FIDU-USDC pool by visiting the [Stake](https://app.goldfinch.finance/stake) tab in the platform, and selecting FIDU, then Migrate, under Stake on Goldfinch.

#### Technical specifications

Implementing the community governance proposal to allow staking FIDU-USDC Curve LP positions for GFI involved augmenting Goldfinch’s [StakingRewards contract](https://etherscan.io/address/0xFD6FF39DA508d281C2d255e9bBBfAb34B6be60c3) to accept FIDU-USDC Curve LP tokens and calculate rewards based on the user’s Curve LP position.

The modifications of the `StakingRewards` contract could enable other types of staked positions on the protocol in the future, should the community pass further proposals to do so. Currently, the `StakingRewards` contract only supports staking FIDU directly, and as such the contract calculates individual rewards based on the amount of FIDU staked. In order to support any potential future community desire for staking tokens in the future, an additional calculation is performed at the time of staking to get the exchange rate used to convert Curve LP tokens to an effective FIDU amount. The exchange rate for a Curve LP position will be calculated using the [virtual price](https://curve.readthedocs.io/factory-pools.html?highlight=virtual#StableSwap.get\_virtual\_price) of the LP token given by Curve.

Note: The Goldfinch protocol uses Curve’s virtual price to calculate the effective FIDU amount instead of spot prices or live ratios of the FIDU-USDC Curve pool to prevent flash loan attacks.

### Senior Pool Liquidity Mining

Participants can earn GFI by staking the FIDU received from supplying capital (USDC) to the Senior Pool. Read our documentation on Senior Pool Liquidity Mining to learn more about the Senior Pool Liquidity Mining’s GFI distribution rate, parameters, and unlock schedule.

Participants can stake their FIDU for GFI by visiting the [Stake](https://app.goldfinch.finance/stake) tab in the platform, and selecting FIDU under Stake on Goldfinch.

Using the Goldfinch protocol application, staked FIDU can also be deposited in the Curve FIDU-USDC pool to earn additional LP rewards without needing to unstake from Goldfinch. To learn more about the community-driven incentives for staking FIDU-USDC Curve LP positions on Goldfinch, read the Staking FIDU-USDC Curve LP Positions section above.

Participants can migrate their staked FIDU to deposit into the Curve FIDU-USDC pool by visiting the [Stake](https://app.goldfinch.finance/stake) tab in the platform, and selecting FIDU, then Migrate, under Stake on Goldfinch.

#### Backer Incentives

To ensure that Backers, who do not receive FIDU in exchange for providing capital to Borrower Pools, are compensated fairly for their participation in the protocol, Backer Staking Rewards are GFI rewards earned by Backers equivalent to the APY from GFI earned by liquidity providers who supply to the Senior Pool and stake their FIDU. Read our documentation on Backer Incentives to learn more about how Backers receive GFI rewards.
