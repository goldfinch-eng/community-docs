# Backer Incentives

The total APY (Annual Percentage Yield) earned by Backers of a Borrower Pool is the sum of three parts:&#x20;

* The **base interest USDC APY** of a Pool’s Junior Tranche is the base-level incentive a Backer can receive from participating in the protocol. This base USDC APY originates from the Borrower’s repayments and is a core feature of the Goldfinch protocol.&#x20;
* **Backer Rewards** are the APY from GFI earned uniquely by Backers, from the Pool’s interest repayments.&#x20;
* **Backer Staking Rewards** are the APY from GFI earned by Backers equivalent to the APY from GFI earned by liquidity providers who supply to the Senior Pool.

In addition to the total APY earned by backers:&#x20;

* **Early Backer Rewards** were an additional GFI reward provided to all Backers who contributed to a Pool prior to the development of the Backer Rewards and Backer Staking Rewards mechanisms.

Backer Rewards and Backer Staking Rewards are functions of the BackerRewards contract. This was passed by community governance to ensure that a Backer’s incentives are always higher than those of a Senior Pool participant’s, in order to preserve the protocol’s consistent risk/reward tradeoff, with Backers, who take on the most risk, rewarded the most highly.

Early Backer Rewards were passed by [community governance](https://gov.goldfinch.finance/t/retroactive-backer-distribution-proposal-4-same-as-3-with-ammendment/505) to retroactively reward Backers of pools that were funded prior to the development of the Backer Rewards and Backer Staking Rewards mechanisms.

Staking on Backers, detailed below, is an element of the [Goldfinch Whitepaper](https://goldfinch.finance/goldfinch\_whitepaper.pdf) and as of April 2022 have not yet been implemented as a live feature on the protocol.

### Early Backer Rewards&#x20;

Backers of pools that were funded before the Backer Rewards and Backer Staking Rewards mechanisms were developed received a one-time airdrop, to reward their early support of the protocol. The parameters of the airdrop were defined in the [proposal](https://gov.goldfinch.finance/t/retroactive-backer-distribution-proposal-4-same-as-3-with-ammendment/505) passed by community governance.

### Backer Rewards&#x20;

Backer Rewards are distributed as GFI rewards to Backers for interest payments made by different Borrowers. For every dollar of interest that a Borrower repays, a Backer will earn an amount of GFI. To incentivize early participation in the protocol, this amount decreases based on the total amount of interest that has been repaid to the Goldfinch protocol as a whole.

The protocol does this to incentivize Backers who are evaluating pools to fully take into account the likelihood that interest payments will be made successfully and on time to the Pool, and to provide an incentive for Backers to hold Borrowers accountable to their obligations.

This means that how much GFI a Backer earns for a dollar of interest is not a fixed value, i.e. at one point in time a Backer may earn a large amount of GFI per dollar of interest, but later in the protocol’s lifecycle they may earn less GFI per dollar of interest. Concretely, the rewards fall off on a square root curve and will eventually fall to 0 once $100MM total dollars of interest has been repaid by Borrowers to the Goldfinch protocol as a whole. As such, Backers who participate in the protocol’s earliest pools will receive more rewards than Backers who take part later on, when the protocol’s usage has grown.

### Backer Staking Rewards&#x20;

Backer Staking Rewards take the form of GFI distributed to Backers in exchange for their role taking on the additional risk of providing first-loss capital to Backer Pools. This is achieved by providing Backers equivalent GFI rewards as if they had deposited and staked in the protocol’s Senior Pool. The protocol does this so that Backers are compensated fairly for the increased risk they take on in the protocol.

Upon a successful repayment from a Borrower, a Backer will be able to claim the full amount of Backer Staking Rewards they've earned since the last time they claimed. Partial repayments made by the Borrower to their Pool do not entitle Backers to rewards, only full payments. However, if a Borrower eventually does make a repayment on their outstanding obligations, Backers will not be penalized and will receive the same rewards as if the incomplete payment never occurred.

Backer Staking Rewards is an implementation of the accepted Goldfinch governance proposal titled "[Backer Participation in Staking Rewards](https://gov.goldfinch.finance/t/backer-participation-in-staking-rewards/682).”

### BackerRewards Contract Technical Design&#x20;

Backer Rewards Interest repayments to a Pool earn GFI for Backers according to the parameters of the approved [backer liquidity mining proposal](https://snapshot.org/#/goldfinch.eth/proposal/0xb716c18c38eb1828044aca84a1466ac08221a37a96ce73b04e9caa847e13e0da). Thus 2% of the total GFI supply is allocated for this purpose, to be earned upon the first $100M of interest repaid to the protocol. GFI are earned at an "exponentially decelerating rate" across all interest dollars repaid to eligible pools; the exact formula can be found in the documentation of the smart contract.

![](https://lh3.googleusercontent.com/fwAIIkW4pZDVFJqi2Cb8Dy3-d\_5Bhw-IZd3qw4jtjd8\_DzwreXvQpiv2DnVvKYI2-G6mV\_jHBetfXCSrmbghKv8phLyvWNd15oUh6PjOMigih9rp7VYxcSSrTPlsBhnaRcqb9C7-)

#### Backer Staking Rewards&#x20;

From the time of drawdown of the Pool's Backer capital, until the term end time of the loan, the protocol calculates an amount of "virtual" FIDU, corresponding to the borrowed amount of capital supplied by the backer, that would have earned the APY-from-GFI of Senior Pool staking, if that amount of FIDU had been staked in the Senior Pool. The backer earns an equivalent\[^1] amount of GFI as they would have earned from staking this amount of “virtual” FIDU in the Senior Pool.

\[^1]: We say "equivalent" rather than "equal" due to a subtlety of implementation in the calculation logic relating to the term end time of the loan.

#### Distribution Parameters&#x20;

The GFI earned from Backer Rewards and Backer Staking Rewards is not subject to a lockup period once it is earned. But the GFI of Backer Rewards and Backer Staking Rewards is only earned by Backers upon an interest repayment to the pool by the Borrower, at which time the earnings from Backer Rewards and Backer Staking Rewards are checkpointed and a corresponding additional amount of GFI since the last checkpoint becomes claimable by backers.

### Staking on Backers&#x20;

Staking on Backers, detailed below, is an element of the [Goldfinch Whitepaper](https://goldfinch.finance/goldfinch\_whitepaper.pdf) which as of April 2022 has not yet been implemented as a live feature on the protocol.

In addition to evaluating individual Borrower Pools, Backers may also evaluate other Backers in order to give them leverage. Backers can do this by staking GFI directly on another Backer. Based on the amount of GFI staked on a given Backer, the Senior Pool uses the Leverage Model to calculate a leverage ratio and allocate capital whenever that Backer supplies to Borrower Pools. For example, if a Backer has a leverage ratio of 4.0X based on who has staked GFI on them, then anytime they supply to a Borrower Pool, the Senior Pool will allocate up to 4.0X of that amount.

The Senior Pool provides this leverage up to a maximum total that is calculated as the leverage ratio multiplied by the total value of GFI staked on that Backer. For example, if the Backer has $1M worth of GFI staked on them with a 4.0X leverage ratio, the Senior Pool will allocate up to $4M total leverage.

When GFI is staked on a Backer, that GFI serves as collateral against potential defaults for that Backer’s positions in Borrower Pools. When a Borrower defaults, the GFI staked on all the Backers in that pool are reallocated to the senior tranche until the senior tranche is made whole on their expected payments. This incentivizes Backers to stake on other Backers who supply to safe Borrower Pools.

To reward Backers for staking GFI on other Backers, the protocol distributes GFI to them on a regular basis. The protocol allocates the distributions in proportion to the interest their leveraged GFI earns. This incentivizes Backers to stake on other Backers who supply to high-yielding Borrower Pools.

### Summary of Backer Incentives&#x20;

Backers have an incentive to provide first-loss capital to Borrower Pools because they can receive both Backer rewards and higher effective yields based on the Senior Pool leverage. To help ensure that Backers are always receiving as much or higher of an APY on their pool participation as Senior Pool Participants, Backer Rewards and Backer Staking Rewards are also distributed based on participation. In the future, Backers will also have an incentive to stake GFI on other Backers as they will be able to earn additional rewards when that Backer supplies to Borrower Pools.
