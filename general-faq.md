# General FAQ

#### **How do I get involved in the Goldfinch community?**

There are several ways to get involved in the Goldfinch protocol. The best ways to get involved in the protocol are:&#x20;

* Participating as an active community member by joining the [Discord.](https://discord.com/invite/HVeaca3fN8)
* Being a Liquidity Provider in the Senior Pool (see[ Liquidity Providers ](protocol-mechanics/liquidityproviders.md)to learn more).
* Being a Backer to Borrower Pools (see [Borrower Pools](broken-reference) to learn more).

#### **Do I need to be an Accredited Investor to participate in the Senior Pool?**

US residents must be Accredited Investors to supply capital to the Senior Pool. Anyone outside of the US within regions supported by UID can participate in the [Senior Pool](guides/participating-in-the-senior-pool.md). To learn how to participate, click [here](guides/participating-in-the-senior-pool.md).

#### **Where can I find the updates of the Goldfinch Protocol?**

You can sign up for weekly Goldfinch Updates on the [Goldfinch Substack](https://goldfinch.substack.com/), or follow along live on [Twitter](https://twitter.com/goldfinch\_fi) and [Medium](https://medium.com/goldfinch-fi). You can connect with the community to stay connected with what's going on in the [Goldfinch Discord](https://discord.com/invite/HVeaca3fN8) server and [Telegram](https://t.me/goldfinch\_finance). To receive live updates when new Borrower Pools are launching, sign up for [Backer Updates](https://finance.us6.list-manage.com/subscribe?u=474a4e1e3558f9c3cf4d6475d\&id=3424bed28d).&#x20;

#### **I don't speak English. Will Goldfinch dapp be available in my language?**

The app is still in English. However, there are different language channels set up in Discord - Russian, Ukrainian, Korean, Turkish, Indonesian, Vietnamese, Spanish, among others. These channels are great for asking any questions, and whenever an announcement goes out in English, these channels share a translated version. Community members have volunteered to translate the content into different languages, and any member should feel empowered to [request](https://docs.google.com/forms/d/e/1FAIpQLSfMo9JSudo0LTGsNG5uKT6bBPtD5hF0Rod7rVlQIXJ9QHnMSw/viewform) to have one, and the community moderators will set it up if there is a high need.

#### **Is Goldfinch a blockchain?**

No, it is not. Goldfinch is built on top of the Ethereum blockchain.

#### **Is Goldfinch open source?**

Yes. All code, including the front-ends can be found at [https://github.com/goldfinch-eng/mono](https://github.com/goldfinch-eng/mono). Just the smart contracts and associated audits can be found here: [https://github.com/goldfinch-eng/goldfinch-contracts](https://github.com/goldfinch-eng/goldfinch-contracts).

#### Does Goldfinch h**ave a Bug Bounty program?**

Yes, Goldfinch has a [Bug Bounty program](https://immunefi.com/bounty/goldfinch/) in partnership with Immunefi.

#### **Which wallets does the dapp support?**&#x20;

The dapp supports [WalletConnect](https://walletconnect.com/), [Metamask](https://metamask.io/), and [Ledger](https://www.ledger.com/ledger-live/download). Ledger performs optimally through [Firefox](https://www.mozilla.org/en-US/firefox/new/). [Trezor](https://trezor.io/) is currently not supported.

#### What is the currency of the loans?

All loans are in USDC. You can learn more about USDC [here](https://www.circle.com/en/usdc).

#### Does Goldfinch really take no collateral in its deals?

Goldfinch does not ask Borrowers to deposit any on-chain collateral to take out a loan. Instead, when structuring a loan, Borrowers pledge real-world assets as collateral.&#x20;

#### **Has the Goldfinch protocol been audited?**

Yes, by [Certik](https://www.certik.com/) and [Trail of Bits](https://www.trailofbits.com/). The initial V2 of the protocol (the design outlined in the white paper) has been audited by Certik (here is the [Github repo](https://github.com/goldfinch-eng/goldfinch-contracts)). Another audit was done by Trail of Bits (https://www.trailofbits.com/) in November 2021 (here is the [Github repo](https://github.com/goldfinch-eng/goldfinch-contracts)).

#### **Who are the current Borrowers using the protocol?**

The list of past borrowers is available publicly [here](https://app.goldfinch.finance/earn) under `Borrower Pools`. The focus right now is on credit funds and later stage borrowers who are series B and beyond.

#### I heard about "Flight Academy," what was that?

Flight Academy was a program that empowered the Backer community with tools and basic vocabulary needed to evaluate Debt Capital Markets deals. The program aimed to establish community values and set community norms. The academy ran from September 20, 2021, to October 25, 2021. The academy tutorials are [available](https://www.youtube.com/watch?v=4hGungwsEQk\&list=PLJsUPOCzOm\_zJ08Mgc0vLs-1pymgcO2\_-) for free. Participants were rewarded with GFI (Goldfinch's token) based on a specific criteria, as explained in the final announcements [here](https://discord.com/channels/793925570739044362/806257997680345188/921477436024168548), and [here](https://discord.com/channels/793925570739044362/806257997680345188/922571454917247036).&#x20;

Currently, the community has not proposed hosting another Flight Academy. However, community members should feel empowered to propose one through governance.&#x20;

#### **Backer Incentives vs. LP Incentives**

There have been a lot of questions about the fact that retroactive distributions happened on launch day (Jan 11th) for LPs and not for Backers. Per the white paper, and because of this community-approved [governance proposal](https://gov.goldfinch.finance/t/backer-participation-in-staking-rewards/682), Backers will now receive distributions for participating in Borrower Pools. The smart contracts for Backer distributions have already been audited and deployed, and are already on the community Github repo [here](https://github.com/goldfinch-eng/mono/blob/main/packages/protocol/contracts/rewards/BackerRewards.sol). \
Read more about [Backer Incentives here](protocol-mechanics/investor-incentives/backer-incentives.md).

#### If a Borrower defaults, is the money paid back on-chain or off-chain?

In practice, there are security agents with each Borrower that are instructed to liquidate the pledged collateral, convert into USDC, and make payments on chain into the relevant Borrower pool. The Senior Pool and Backers are then able to claim their portion of the funds from the Borrower pool.

#### What sort of deals can the Goldfinch protocol be used for?

Almost any kind of credit-related investment, into a real-world venture providing some sort of productive service. The Goldfinch protocol is a marketplace, where capital is aggregated for various use cases as it relates to lending. The transaction sponsor (e.g. borrower, or lead backer) owns presenting an opportunity to the community (e.g. principal investment into a corporate, credit fund co-investment, credit fund sub-participation etc...), with the community, ultimately deciding whether or not to fund the opportunity.

#### What type of structured facility can the Goldfinch protocol provide **Borrowers**?

The protocol provides a uni-tranche facility, whereby a single credit line is made available, at a single coupon. There is no ability to only raise junior, or senior capital through the Goldfinch protocol.

#### How can I assess whether the Smart Contract which governs how capital moves works?

The smart contract code is freely accessible and can be found in Github. The Goldfinch smart contract has additionally been audited by 3rd party providers for security flaws by teams like Trail of Bits. You can learn more about the smart contract and Goldfinch's code in the [Developer Documentation](https://dev.goldfinch.finance/).&#x20;

#### **Bots are immediately withdrawing as new money comes in! Can you stop this? What's going on?**

In times of very low excess liquidity in the Senior Pool, LP holders don't have the ability to exit their positions from the pool directly, so they turn to the secondary markets (like [Curve](https://curve.exchange/ethereum/pools/factory-crypto-23/swap/)) to sell their position. This can mean FIDU sells at a discount on those markets until more liquidity comes into the pool. &#x20;

This discount creates an opportunity for arbitrage bots to pull out the new deposits and repayments as soon as they come in (by buying discounted FIDU on the secondary, and selling it to the pool at the higher, native price). If you're an LP who isn't running a bot, and you want to exit, this can be frustrating, and so some people have asked that the community "do something" about it. Stop the bots in some way, thinking that this may stop the issue.&#x20;

While certain new mechanics could help, it's important to remember 1.) No one can really stop someone from running a bot, and 2.) the bots are **an effect, not a cause of low liquidity**. So stopping them wouldn't really change the situation.&#x20;

The secondary markets give LPs with the most need for liquidity the ability to exit now (at the expense of slippage), even when "native" liquidity isn't available. **The secondary markets do not fundamentally change the withdraw pressure**. They just create a market pricing mechanism for who is willing to "pay the most" for the ability to exit now.

While eventually borrower repayments would cover everyone in the Senior Pool, the best overall solution is to continue to drive new liquidity to the pool. Once the arb opportunity closes, then any new liquidity will stay there and arb bots will not continue.

#### What is in the Important Links section of the documentation?

* [Governance Portal](https://gov.goldfinch.finance/): The site for Goldfinch's Governance proposals and Discussions. You can learn more about the Governance process in the [Governance section](governance.md) of the documentation.
* [Developer Documentation](https://dev.goldfinch.finance/): A documentation site for developers and those auditing Goldfinch's code, for a deeper technical dive into Goldfinch’s code, smart contract configuration, security, and other technical features.&#x20;
* [Protocol Data Dash](https://dune.com/goldfinch/goldfinch)board: A Dune dashboard providing live insights into the Goldfinch protocol, including 30 day protocol revenue, repayment metrics, defaults, and more.&#x20;
* [November 2021 Audit](https://github.com/goldfinch-eng/goldfinch-contracts): A link to the second protocol external protocol audit, completed by Trail of Bits.&#x20;
* [Immunefi Bug Bounty](https://immunefi.com/bounty/goldfinch/): The bounty for developer bug detection, focused on preventing code impacts such as loss of user funds and hosted by Immunefi.&#x20;
* [Github](https://github.com/goldfinch-eng): The open-source repository for all of Goldfinch's code.&#x20;

