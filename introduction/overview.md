# Goldfinch Overview
---

## Participants

?> The Goldfinch protocol has four core participants: Borrowers, Backers, Liquidity
Providers, and Auditors.

**Borrowers** are participants who seek financing, and they propose Borrower Pools for
the Backers to assess. Borrower Pools contain the terms a Borrower seeks, like the
interest rate and repayment schedule.

**Backers** assess the Borrower Pools and decide whether to supply first-loss capital. After
Backers supply capital, Borrowers can borrow and repay through the Borrower Pool.

**Liquidity Providers** supply capital to the Senior Pool in order to earn passive yield. The
Senior Pool uses the Leverage Model to automatically allocate capital to the Borrower
Pools, based on how many Backers are participating in them. When the Senior Pool
allocates capital, a portion of its interest is reallocated to the Backers. This increases
the Backers’ effective yield, which incentives them to both provide the higher-risk
first-loss capital and do the work of assessing Borrower Pools.

Lastly, **Auditors** vote to approve Borrowers, which is required before they can borrow.
Auditors are randomly selected by the protocol, and they provide a human-level check
to guard against fraudulent activity.

## Architecture Diagram
<table>
<tr>
<td align="center">
<img src="https://goldfinch.finance/images/how-it-works-1.png">
<img src="https://goldfinch.finance/images/how-it-works-2.png">
<img src="https://goldfinch.finance/images/how-it-works-3.png">
<br />
</td>
</tr>
</table>

## Glossary of Core Components
> - Auditors — Participants who receive GFI rewards for securing the protocol with
a human eye.
> - Backers — Participants who supply junior tranche (first-loss) capital to
individual Borrower Pools.
> - Borrowers — Participants who raise capital from the protocol via Borrower
Pools.
> - Borrower Pool — Smart contract that encodes a set of financing terms for a
Borrower, including the interest rate and repayment schedule, and through
which the Borrower can borrow capital and repay it with those terms.
> - GFI — Token used for Governance votes, Auditor staking, Auditor vote rewards,
staking on Backers, early Backer rewards, and other potential rewards for all
protocol participants.
> - Governance — Smart contract that is managed by the community DAO and has
the ability to update the protocol via decentralized governance votes.
> - Leverage Model — A formula by which the Senior Pool automatically determines
how much capital to allocate to each Borrower Pool.
> - Liquidity Providers — Participants who supply capital to the Senior Pool.
> - Senior Pool — Smart contract that accepts capital from Liquidity Providers and
automatically allocates capital to the senior tranche of Borrower Pools according
to the Leverage Model.
    


