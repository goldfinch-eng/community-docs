# Borrowers

{% hint style="success" %}
Borrowers are participants who seek financing from the protocol. They propose terms to Backers to supply capital to their Borrower Pools.
{% endhint %}

## Borrower Pool creation

A Borrower Pool is the smart contract through which Borrowers borrow and repay capital. Once approved by Auditors, any Borrower can create a Borrower Pool and define the terms they want:&#x20;

* **Interest Rate**: Fixed interest rate APR, e.g. 15%.&#x20;
* **Limit**: Total capital that can be borrowed, e.g. $10M.&#x20;
* **Payment Frequency**: Frequency of interest and principal payments, e.g. every 30 days.
* **Term:** The length of time until the full principal is due, e.g. 365 days.&#x20;
* **Late Fee**: Additional interest owed when payments are late, e.g. 5%.&#x20;

Creating a Borrower Pool is like proposing a “term sheet” to Backers. It does not guarantee the terms will be accepted, since Borrowers then need to convince Backers to supply junior tranche (first-loss) capital to the Pool. The amount Borrowers can borrow is based on how much Backers supply, combined with the correlated amount the Senior Pool allocates based on the Leverage Model.

Notably, Borrowers need to set a limit for their Borrower Pools: a self-imposed cap on how much capital they can borrow, also referred to as the Pool limit. While Borrowers might ideally want an infinite limit, Backers want to know that they are only staking first-loss capital toward a total potential amount that the Borrowers can safely deploy. Borrowers therefore have an incentive to set the limit only as high as they can convince Backers that they can safely use and repay.

In order to create a Borrower Pool, the Borrower must also stake an amount of GFI equal to double the cost of an Auditor approval, which is a fixed rate set by the protocol and determined by community governance. This helps guard against spam, signals to Backers that the Borrower is serious, and provides GFI to pay for the first Auditor approval. The first half of the staked GFI is used for the first Auditor approval. The Borrower can redeem their remaining staked GFI when they have fully repaid their borrowed balance.

## Borrowing and repaying

Borrowers can borrow capital through the Borrower Pool at any time. The total amount they can borrow is the minimum of:&#x20;

A. The calculated limit based on the capital that Backers have supplied and the capital automatically allocated by the Senior Pool according to the Leverage Model.&#x20;

B. The combined total capital that Backers have supplied in that Borrower Pool plus the remaining capital in the Senior Pool.&#x20;

C. The Borrower Pool's limit.

After borrowing, Borrowers make repayments to the Borrower Pool according to its interest rate and payment period. When they pay more than the interest owed, the remainder is applied to the principal balance.

## Junior and senior tranches <a href="#juniorseniortranches" id="juniorseniortranches"></a>

Borrower Pool smart contracts have both a junior and senior tranche. Backers supply capital directly to the junior tranche, and the Senior Pool supplies capital to the senior tranche. When a Borrower makes repayments, the Borrower Pool applies the amount first toward any interest and principal owed to the senior tranche at that time, and then toward any interest and principal owed to the junior tranche at that time.

To track the different amounts that different participants supply, both the Backers and the Senior Pool receive an NFT when they supply capital. The NFT tracks the amount that was supplied and how much of it has been redeemed. At any time, a Backer or the Senior Pool can use their NFT to redeem their specific portion of the available repayments in the Pool.

The Borrower Pools use NFTs rather than fungible tokens because it allows the protocol to ensure that no one redeems more than their proportional share of the total repayments as they come in.

For example, let’s say two Backers have each supplied $500 for a total of $1,000 borrowed, and that so far the Borrower has made repayments totaling $300. In this scenario, the NFTs ensure each Backer can only redeem up to $150, which is their portion of the repayments so far, rather than each one racing to redeem the full $300 for themselves.

## Origination fee

There may be certain participants who work with Borrowers to establish terms and bring them to the protocol. To compensate them for these efforts, Borrower Pools support an origination fee that is paid to the Pool's originator.

The origination fee is defined as a percentage of the interest. For example, for a $1M Borrower Pool with 15% interest paid monthly and a 10% origination fee, the Borrower would pay monthly interest of $12.5K and the originator would receive a monthly fee of $1.25K. To align incentives with Investors, the originator fee is treated as the most junior tranche, so every payment first goes toward what is owed to the Senior Pool (senior tranche) and Backers (junior tranche) before it goes toward the originator fee.

## Borrower repayment incentives

{% hint style="success" %}
A key question is what incentives Borrowers have to pay back what they borrow
{% endhint %}

The first incentive is the establishment of a positive on-chain credit history. Because Borrowers need to publicize their wallet address when proposing pools to Backers, their on-chain history becomes public to future creditors—even those off-chain. As more of global finance moves on-chain, creating a negative on-chain credit history is comparable for future credit opportunities to creating a negative off-chain credit score or record.

The second incentive is that Borrowers will likely want to continue borrowing from Goldfinch. The moment they are late on any payment, Borrowers are unable to borrow further from any Borrower Pool.

While not explicitly supported by the protocol, a third incentive is that Backers may form off-chain legal agreements with Borrowers, including requiring Borrowers to collateralize their on-chain loan with off-chain collateral. Backers may require such an agreement to be in effect, either with them directly or with another Backer, in order to be willing to supply capital. In these cases, the legal agreement and potential Investor recourse are another important incentive for Borrowers. Currently, all loans on Goldfinch are fully collateralized with off-chain assets via this mechanism.

In addition, while occasional defaults are common across finance, Backers will likely stop supplying more capital to any of a Borrower’s pools if the Borrower is consistently late on repayments. It is up to Backer to evaluate whether Borrowers are qualified and have a good enough track record to garner Backer investment in any future pools the Borrower proposes.
