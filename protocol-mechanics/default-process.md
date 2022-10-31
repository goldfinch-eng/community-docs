---
description: >-
  What triggers a Borrower Pool to enter default status, and the process that
  follows.
---

# Default Process

All parameters for the default process are defined in the off-chain legal agreements established per Borrower Pool, in addition to being defined in the Pool’s smart contract.

Borrowers provide performance reporting (e.g. covenant compliance, asset quality performance) directly to their Investors via the [Borrower Communication tooling](https://medium.com/goldfinch-fi/facilitating-more-transparency-between-borrowers-and-investors-on-goldfinch-890fa9c13832), which also allows Investors to engage directly with Borrowers throughout any default process that may take place.

1. Borrowers make monthly interest payments to their Pools to service their debt, as defined in the Pool terms.
2. When a Borrower misses an interest payment date, defined by their off-chain agreement, or breaks any other provision in their off-chain agreement:&#x20;
   * **Off-chain**: Borrower enters a 3-7 (exact dates vary by pool according to what investors negotiated for) grace period to remediate the missed payment, or broken provision.&#x20;
   * **On-chain**: Borrower enters a 45 day grace period before the protocol marks the loan on-chain as being in default, and starts provisioning the loan.
3. After 45 days of non-payment, the loan officially enters default status on-chain.&#x20;
   * The Pool is now subject to its default interest rate as defined in the Pool terms:&#x20;
     * For **Senior Pool investors**, the value of the loan will on a daily linear basis, be automatically written down over 120 days. If repayments are eventually made, then the writedown will be reversed accordingly.&#x20;
     * For **Backers** in a given pool, no writedown mechanics are necessary since there is already a defined waterfall and pro rata distribution.&#x20;
   * Investors work with the Borrower via Borrower Communication channels or off-chain methods to identify the conditions leading to the default, remediate and agree to a repayment plan, and establish transparent solutions to move forward with future repayments.
   * Any partial payments to the Pool are distributed first to the Senior Pool (senior tranche debt) and then to Backers (junior tranche debt).
4. If the remediation process is not successful, Goldfinch Investors will be able to pursue off-chain legal recourse via any on and off-chain overcollateralization the Borrower had provided in order to recoup losses.&#x20;
   * Currently, all Pools on Goldfinch are fully collateralized with off-chain assets.&#x20;
