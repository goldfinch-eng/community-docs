# Auditors


{% hint style="success" %}
Auditors perform human-level checks on Borrowers to confirm they are legitimate, helping to secure the protocol against fraud. Borrowers need the approval of Auditors to borrow from Borrower Pools.
{% endhint %}

## Approval Votes

Borrowers need an approval vote from Auditors in order to borrow. Auditors stake GFI in order to be selected for votes, and they earn GFI rewards when they vote with the majority of other Auditors, according to the rules described below.

* Anyone can be an Auditor by staking a minimum amount of GFI and passing the

  Unique Entity Check. When a vote is requested, the protocol selects 9 Auditors on a

  random basis weighted by the amount of GFI they have staked.

* When selected for a vote, Auditors evaluate whether Borrowers appear to be legitimate.

  In this vote, the Auditors are not evaluating the Borrower’s creditworthiness — rather,

  they are providing a confirmation that the Borrower does what they claim to do and

  that they do not appear to be colluding with any other participants.

* Auditors can do whatever they like to decide how to vote. In practice, they may review

  off-chain documents provided by Borrowers and communicate with Borrowers directly

  through channels such as forums, email, and video calls. This can all occur off-chain on

  a variety of platforms. The protocol only needs the final vote and is agnostic to how

  Auditors arrive at their vote.

## Approval Vote Requests

Borrowers can request an approval vote once their first Borrower Pool has reached at least 20% of its limit and they have staked enough GFI to reward Auditors for the vote. If more than 2 Auditors vote “No”, their full GFI staked amount is slashed.

In addition to the Borrower making their first approval request, anyone can use GFI to pay for an approval request at any time. This is helpful if someone believes a prior approval vote had an incorrect result, or if someone believes the Borrower has started to act fraudulently and should lose their approval.

## Approval Vote Outcomes

Once selected, auditors have 48 hours to provide a `Yes`, `Unsure`, or `No` vote. Their GFI is slashed if they:

* don’t vote within the 48 hour window, 
* vote `Yes` when the majority vote `No`, or 
* vote `No` when the majority vote `Yes`.


{% hint style="danger" %}
If they vote `Unsure`, there is no penalty but also no reward.
{% endhint %}

Based on the way Auditors vote, there are three potential outcomes: 

1. **Full Approval:** This occurs when there are at least 6 `Yes` votes and no more than 1 `No` vote. The Borrower is approved to access capital, and the Senior Pool allocates capital to their Borrower Pools. 

2. **Backer-Only Approval:** This occurs when there are at least 6 `Yes` or `Unsure` votes, and no more than 1 `No` vote. The Borrower is approved to access capital, but the Senior Pool does not allocate capital to their Borrower Pools. 

3. **No Approval:** This occurs when there is more than 1 `No` vote, or when there are not enough votes to meet the above approval thresholds. The Borrower is not approved to access any capital.


## Summary of Auditor Incentives

Auditors are incentivized to participate and vote correctly in order to earn GFI rewards. Also, by staking GFI, they are both incentivized to avoid having their stake slashed and are naturally aligned with the long term success of the protocol.

