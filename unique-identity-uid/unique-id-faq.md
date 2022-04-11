---
description: >-
  For greater support, head over to the Discord server linked under the
  Important Links section.
---

# Unique ID FAQ

#### What happens if I lose access to my UID? Can UID be reissued to a new wallet address?&#x20;

Currently, it cannot. Burning and reissuing tokens is possible on the smart contract, though this has not been implemented on the front-ends. Theoretically, upon burn, the KYC/KYB/accreditation information would need to be deleted and then members could sign up with a new wallet.

#### Do I need to undergo verification for deposit and withdrawal in both the Senior Pool as well as Borrower Pools?&#x20;

Yes, this is mandatory. UID is the first NFT for identity. No personally identifiable data is stored on-chain. More on UID here.

#### How can I verify my identity?&#x20;

Before minting UID NFT, you need to verify your Ethereum address from here: https://app.goldfinch.finance/verify. Please head over to the Tutorials section for a detailed explanation.

#### How do I know whether I am verified?&#x20;

You can go back to https://app.goldfinch.finance/verify and sign in. If you are verified, you will see the message - “Your address verification is complete” or “Your verification was approved to immediately access the Senior Pool”.

#### Why do the Backers need to verify their identity/be KYC'd?&#x20;

The protocol must have sybil resistance in order to implement the "trust through consensus" mechanism outlined in the whitepaper. Technically, this does not need to be KYC, and the community hopes to offer versions of this in the future which do not require ID verification. However, KYC offers sybil resistance as well as the legal compliance which many of the Borrowers require for their own purposes.

Note, Goldfinch's KYC/KYB and accreditation is handled by third parties, Persona and [Parallel Markets](https://bridge.parallelmarkets.com/goldfinch), who, like Goldfinch, take privacy and security [very seriously](https://support.withpersona.com/hc/en-us/articles/360057452513-Security-privacy-and-compliance-overview).

#### Is UID interoperable with other protocols?&#x20;

UID is completely interoperable. It is a standard ERC-1155 contract, so any protocol can get the benefits without having to build their own KYC flow or handle any data themselves. If you are a builder, check out the docs here to learn how to integrate it.

#### Can I transfer my UID to others or can I sell my UID on OpenSea?&#x20;

Because the UID is an ERC-1155 contract, it is not transferable and cannot be sold.
