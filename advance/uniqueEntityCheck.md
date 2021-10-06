# Unique Entity Check
---
Since the Leverage Model relies on "trust through consensus", it is critical to avoid sybil
attacks by having confidence that each Borrower, Backer, and Auditor is a unique entity.
Therefore, they must each be verified with a `Unique Entity Check` before they can
participate.

Governance approves the protocol's Unique Entity Check providers. This will start with
oracles that perform off-chain checks to validate that the wallet addresses are unique
entities. However, this design does not require oracles. If and when on-chain
decentralized IDs mature, Governance can vote to migrate the protocol to these new
providers.