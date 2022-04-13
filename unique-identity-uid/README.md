# Unique Identity (UID)

Unique Identity (UID) is a non-transferrable NFT representing Know-Your-Customer (KYC), Know-Your-Business (KYB), and/or U.S. investor accreditation verification on-chain. It is the first NFT for identity. It follows ERC-1155 standards, and is freely usable by any other protocol. No personally identifiable data is stored on-chain.

Know-Your-Customer verification is a check that ensures a person is actually who they say they are, and Know-Your-Business verification is a check that ensures an entity and its representatives are actually who they say they are. Doing so is a legal requirement that prevents cases of fraud and any suspicious activities from occurring on the Goldfinch protocol.

U.S. investor accreditation is for U.S.-based individuals and entities who want to participate in the protocol. Under U.S. federal security laws, only persons who are accredited investors may participate in certain financial opportunities.

There are currently 5 types of UIDs:

1. ID\_TYPE = 0, Non-U.S. Individual: can vote and supply capital across the protocol&#x20;
2. ID\_TYPE = 1, U.S. Accredited Individual: can vote and supply capital to the Senior Pool, and to Borrower Pools on a case-by-case basis (depending on Borrowers’ requirements)&#x20;
3. ID\_TYPE = 2, U.S. Non-Accredited Individual: can vote, but cannot supply capital&#x20;
4. ID\_TYPE = 3, U.S. Accredited Entity: can vote and supply capital to the Senior Pool, and to Borrower Pools on a case-by-case basis (depending on Borrowers’ requirements)&#x20;
5. ID\_TYPE = 4, Non-U.S. Entity: can vote and supply capital across the protocol

### Why this matters&#x20;

Having an on-chain representation of personhood achieves two major unlocks: It opens DeFi to an entirely new set of real-world participants, notably companies and financial institutions. It greatly expands the design space for new features and mechanisms on DeFi protocols.

Many companies today don’t interact with DeFi due to KYC/KYB and counterparty concerns. But UID solves these issues for them. Many companies are already [borrowing through Goldfinch](https://app.goldfinch.finance/earn), and they wouldn’t be able to without the KYC/KYB and accreditation verifications. As companies grow comfortable with crypto, they could drive an incredible amount of new volume to DeFi protocols.

UID is completely interoperable with the rest of DeFi. It is a standard ERC-1155 contract, so any protocol can get the benefits without having to build their own KYC flow or handle any data themselves. If you’re a builder, go to the [Developer docs](https://docs.goldfinch.finance/goldfinch/unique-identity-uid/for-developers) to learn more.

It’s also important to emphasize that UID seriously factors in privacy. No personally identifiable data is stored on-chain. Goldfinch has partnered with [Persona](https://withpersona.com) to manage the KYC process and data, and with [Parallel Markets](https://parallelmarkets.com) to manage the KYB and accreditation processes and data. They both offer [industry-leading privacy and security practices](https://withpersona.com/security) that are trusted by many of the largest technology companies. Learn more [here](https://medium.com/goldfinch-fi/introducing-unique-identity-uid-the-first-nft-for-identity-830a89207509).

### How it works&#x20;

#### For Non-U.S. Individuals and U.S. Non-Accredited Individuals

When a user completes their KYC process, Persona checks that they have a valid identity and are not a duplicate of other ones. Once verified by Persona, the user is eligible to get his or her UID.

#### For Entities (Non-U.S. and U.S.)

When a user submits their KYB information, Parallel Markets checks that they have valid entity documentation and valid business owners. Once verified by Parallel Markets, an entity is eligible to get its UID.

#### For U.S. Accredited Investors

In addition to submitting KYC information to Parallel Markets, a user also submits information to prove his or her accreditation qualification(s). Parallel Markets checks that they have a valid identity, are not a duplicate of other identities, and that accreditation documents are valid. Once verified by Parallel Markets, the user is eligible to get his or her UID.

#### For all

Once eligible to get a UID, the user submits an Ethereum transaction that mints the UID, which is a non-transferrable NFT that is sent to their address.

There is a 0.00083 ETH fee (about $3) in addition to gas, in order to cover the cost of Persona’s service.

Then, when the user participates in protocols like Goldfinch, these protocols can check that they have this UID, ensuring they are unique and KYC’ed, KYB’ed, or accredited.&#x20;

### About the artist&#x20;

The amazing illustration for UID was created by [Marcelo Meijome](http://marcelo-meijome.com). You can see some of his other [NFT works on Foundation](https://foundation.app/@marcelomeijome).
