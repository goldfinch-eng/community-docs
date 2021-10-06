# Discussion of Fraud Resistance
---
Because the protocol does not require crypto overcollateralization, this opens up new
potential vectors for fraud. It is worth discussing each one in depth, and how the
protocol builds resistance against it. Note that these scenarios focus on malicious or
dishonest activity, not poor performance of well-intentioned borrowing.

## Fraudulent Borrower, Honest Backers
A fraudulent Borrower could attempt to fool both Auditors and Backers into thinking
they are legitimate, and then borrow capital without repaying it. The first guard against
this are the Auditors, who must approve Borrowers before borrowing. Because Auditors
are randomly selected, it is difficult to collude with them. The second guard are the
Backers, who are highly incentivized to analyze their investments closely, since they
supply higher-risk junior capital. It is likely that Backers will want to do extra research
on Borrowers and potentially communicate with them directly. Lastly, Backers may
sign off-chain legal contracts with Borrowers, which opens Borrowers to legal recourse.

## Borrower Collusion with Backers
A Borrower could collude with people they know to act as Backers and supply to their
Borrower Pool. This would artificially increase the leverage ratio and fool the Senior
Pool into allocating additional capital. The first guard against this are the Auditors, who
must approve Borrowers before borrowing. Because Auditors are randomly selected, it
is difficult to collude with them. The second guard is that it requires many individually
verified Backers to supply significant amounts of upfront capital in order for the Senior
Pool to provide leverage, which makes such collusion difficult and expensive. Lastly, the
Unique Entity Check adds sybil resistance by making it difficult to programmatically
create fake Backers.

## Borrower Collusion with Auditors
A Borrower could collude with Auditors to obtain approval for creating Borrower Pools
when they are not legitimate. The first guard is that the Unique Entity Check prevents a
sybil attack where fake Auditors are programmatically created. The second guard is
that Auditors must stake GFI, which is slashed if they vote differently than the majority
of Auditors. The third guard is that Auditors are randomly selected, weighted by their
staked GFI, so it would require staking a significant amount of upfront capital to be
chosen enough to skew the votes. The fourth guard is that anyone can request an
approval at any time, so it would require colluding for all potential future votes rather
than just one. Lastly, even if a fraudulent borrower successfully colludes with Auditors,
they must also convince many Backers to risk their own capital.

## Fraudulent Backers, Honest Borrowers
An individual or group of Backers might supply to a particular Borrower Pool even
when they don’t view it as a good risk. This would artificially increase the leverage ratio
and fool the Senior Pool into allocating additional capital, boosting the Backers'
returns. The first guard against this is that the Unique Entity Check requires each
Backer to be verified, preventing a sybil attack and requiring the coordination of many
people. The second guard against this is that it requires the Backers to take real risk by
supplying first-loss capital. The Backers only achieve higher returns if the Borrower
does in fact pay back what they borrow, in which case it is beneficial to all participants
in the protocol, including the Senior Pool.