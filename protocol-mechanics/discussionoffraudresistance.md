# Discussion of Fraud Resistance

Because the protocol does not require crypto overcollateralization, new potential vectors for fraud are possible. It is worth discussing each one in depth, and how the protocol builds resistance against it. Please note that these scenarios focus on malicious or dishonest activity, not poor performance of well-intentioned borrowing.

## Fraudulent Borrower, honest Backers

A fraudulent Borrower could first attempt to fool both Auditors and Backers into thinking they are legitimate, and then borrow capital without repaying it.&#x20;

The first guard against this are the Auditors, who must approve Borrowers before borrowing. Because Auditors are randomly selected, it is difficult to collude with them.&#x20;

The second guard are the Backers, who are highly incentivized to analyze their investment choices closely as they supply higher-risk junior capital—meaning they will be the last to be repaid if a Borrower was to default. It is likely that Backers will want to do extra research on Borrowers and potentially communicate with them directly.&#x20;

Lastly, Backers may sign off-chain legal contracts with Borrowers, which opens Borrowers to legal recourse. Currently all loans on Goldfinch are fully collateralized with off-chain assets and legal contracts.&#x20;

## Borrower collusion with Backers

A Borrower could collude with people they know to act as Backers and supply to their Borrower Pool. This would artificially increase the leverage ratio and fool the Senior Pool into allocating additional capital.&#x20;

The first guard against this are the Auditors, who must approve Borrowers before they are able to borrow. Because Auditors are randomly selected, it is difficult to collude with them.&#x20;

The second guard is that it requires many individually verified Backers to supply significant amounts of upfront capital in order for the Senior Pool to provide leverage, which makes such collusion with Backers difficult and expensive.&#x20;

Lastly, the Unique Entity Check adds Sybil Resistance by making it difficult to programmatically create fake Backers.

## Borrower collusion with Auditors

A Borrower could collude with Auditors to obtain approval for creating Borrower Pools when the Borrower is in fact not legitimate.&#x20;

The first guard against this is that the requirement of a Unique Entity Check prevents a Sybil Attack, where fake Auditors are programmatically created to overwhelm the system. Instead, each Auditor must be a verified entity.&#x20;

The second guard is that Auditors must stake GFI in order to participate, which is slashed if they vote differently than the majority of Auditors. This incentivizes Auditors to act honestly in order to preserve their stake.

The third guard is that Auditors are randomly selected, weighted by their staked GFI, so it would require staking a significant amount of upfront capital to be chosen frequently enough to skew the votes.&#x20;

The fourth guard is that anyone can request an approval at any time, so it would require colluding for all potential future votes rather than just one.&#x20;

Lastly, even if a fraudulent borrower successfully colludes with Auditors, they must also convince many Backers to risk their own capital by depositing to the Pool.&#x20;

## Fraudulent Backers, honest Borrowers

An individual or group of Backers might supply to a particular Borrower Pool even when they don’t view it as a good risk. This would artificially increase the leverage ratio and fool the Senior Pool into allocating additional capital, boosting the Backers' returns.&#x20;

The first guard against this is that the Unique Entity Check requires each Backer to be verified, preventing a Sybil Attack of programmatically-created Backers and instead requiring the coordination of many people to achieve Backer collusion.&#x20;

The second guard against this is that it requires the Backers to take real risk by supplying first-loss capital. The Backers only achieve higher returns if the Borrower does in fact pay back what they borrow, in which case it is beneficial to all participants in the protocol, including the Senior Pool.
