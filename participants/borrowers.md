# Borrowers
---
?>Borrowers are participants who seek financing from the protocol. They propose
terms to Backers to supply capital to their Borrower Pools.

## Borrower Pool Creation
A Borrower Pool is the smart contract through which Borrowers borrow and repay
capital. Any Borrower can create a Borrower Pool and define the terms they want:

- Interest Rate: Fixed interest rate APR, e.g. 15%.
- Limit: Total capital that can be borrowed, e.g. $1M.
- Payment Period: Frequency of interest payments, e.g. every 30 days.
- Term: When the full principal is due, e.g. 365 days.
- Late Fee: Additional interest owed when payments are late, e.g. 5%.

Creating a Borrower Pool is like proposing a “term sheet” to Backers. It does not
guarantee the terms will be accepted, since Borrowers then need to convince Backers
to supply junior tranche (first-loss) capital. The amount Borrowers can borrow is based
on how much Backers supply, combined with the amount the Senior Pool allocates
based on the Leverage Model.

Notably, Borrowers need to set a limit for their Borrower Pools, a self-imposed cap on
how much capital they can borrow. While Borrowers might ideally want an infinite
limit, Backers want to know that they are staking first-loss capital only towards a total
potential amount that the Borrowers can safely deploy. Borrowers therefore have an
incentive to set the limit only as high as they can convince Backers they can safely use.

In order to create a Borrower Pool, the Borrower must also stake an amount of GFI
equal to double the cost of an Auditor approval, which is a fixed rate set by the protocol.
This helps guard against spam, signal to Backers that the Borrower is serious, and
provide GFI to pay for the first Auditor approval. The first half of the staked GFI is used
for the first Auditor approval. The Borrower can redeem their remaining staked GFI
when they have fully repaid their borrowed balance.

## Borrowing and Repaying
Borrowers can borrow capital through the Borrower Pool at any time. The total amount
they can borrow is the minimum of:

> A. The calculated limit based on the capital that Backers have supplied and the
additional Senior Pool leverage amount.
>
> B. The combined total capital that Backers have supplied in that Borrower Pool plus
the remaining capital in the Senior Pool.
>
> C. The Borrower Pool's limit.

After borrowing, Borrowers make repayments to the Borrower Pool according to its
interest rate and payment period. When they pay more than the interest owed, the
remainder is applied to the principal balance.

## Junior and Senior Tranches
Borrower Pools have both a junior and senior tranche. Backers supply capital to the
junior tranche, and the Senior Pool supplies capital to the senior tranche. When a
borrower makes repayments, the Borrower Pool applies the amount first toward any
interest and principal owed to the senior tranche at that time, and then toward any
interest and principal owed to the junior tranche at that time.

To track the different amounts that different participants supply, both the Backers and
the Senior Pool receive an NFT when they supply capital. The NFT tracks the amount
that was supplied and how much of it has been redeemed. At any time, a Backer or the
Senior Pool can use their NFT to redeem their specific portion of the available
repayments in the pool.

The Borrower Pools use NFTs rather than fungible tokens because it allows the protocol
to ensure that no one redeems more than their proportional share of the total
repayments as they come in. For example, let’s say two Backers have each supplied $500
for a total of $1,000 borrowed, and that so far the Borrower has made repayments
totaling $300. In this scenario, the NFTs ensure each Backer can only redeem up to
$150, which is their portion of the repayments so far, rather than each one racing to
redeem the full $300 for themselves.

## Origination Fee
There may be certain participants who work with Borrowers to establish terms and
bring them to the protocol. To compensate them for these efforts, Borrower Pools
support an origination fee that is paid to the pool's originator. The origination fee is
defined as a percentage of the interest. For example, for a $1M Borrower Pool with 15%
interest paid monthly and a 10% origination fee, the Borrower would pay monthly
interest of $12.5K and the originator would receive a monthly fee of $1.25K. To align
incentives with capital providers, the originator fee is treated as the most junior
tranche, so every payment first goes toward what is owed to the senior pool and backers
before it goes toward the originator fee.

## Summary of Borrower Incentives
?> A key question is what incentives Borrowers have to pay back what they borrow.

The first incentive is that Borrowers likely want to continue borrowing from Goldfinch.
The moment they are late on a payment, Borrowers are unable to borrow further from
any Borrower Pool. Also, Backers will likely stop supplying more capital if a Borrower is
continually late on repayments. It is up to Backers to determine that Borrowers do in
fact want to continue borrowing from the protocol in the future.

The second incentive is that because Borrowers need to publicize their address when
proposing pools to Backers, their on-chain history becomes public to future creditors,
even those off-chain.

Lastly, while not explicitly supported by the protocol, Backers may form off-chain legal
agreements with Borrowers. Backers may require such an agreement to be in effect,
either with them directly or with another Backer, in order to be willing to supply
capital. In these cases, the legal agreement and potential recourse are another
important incentive for Borrowers.