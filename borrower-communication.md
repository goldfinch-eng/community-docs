---
description: >-
  Tooling to facilitate communications between Borrowers and Investors on
  Goldfinch
---

# Borrower Communication

In response to demand for more efficient channels of communication between Investors and the Borrowers on the protocol, the community introduced standardized channels to allow Borrowers to share updates on their pools and to communicate directly with the protocol’s Investors.&#x20;

This new Borrower Communications tooling is the first of its kind to use web3 solutions for investor reporting, and provides even more transparency for Goldfinch Investors by providing them with easy access to information like:

* Trusted, secure, real-time communication channels between Borrowers and Investors
* Accessible way for Borrowers to fulfill any and all obligatory Investor Reporting requirements, creating easier inroads to access the reporting that exists in their off-chain documents and agreements&#x20;
* More effective channels for Investors to securely communicate with one another, enabling enhanced collective bargaining power.

For each Borrower Pool on Goldfinch, there will be two channels launched:

1. A **token-gated Discord channel** where the Borrower can communicate with Investors  (both Backers and Senior Pool LPs) to provide updates, and where Investors can discuss the Pool amongst themselves. This will be managed by the Goldfinch community.
2. A **password-gated Dataroom** where Borrowers will post all necessary documents that they are obliged to provide as part of their off-chain legal agreements with Investors for compliance, reporting, and evaluation. This will be managed by the Borrower in line with what their existing real-world agreements require.

Each channel has a unique configuration to ensure that Investors are able to easily access the differing levels of information they need from Borrowers, while ensuring the confidentiality of the Borrowers’ proprietary information is accommodated.

### Channel #1: token-gated Discord channel

For every Borrower Pool on the Goldfinch protocol, there will be a **community-managed** Discord channel launched in the[ Goldfinch Discord](https://discord.gg/keH5tZSc). This channel will be configured to permit access for:

* Backers invested in the Borrower Pool in question, who possess at least one pool token representing the Backer’s participation in the Borrower Pool&#x20;
* Liquidity Providers in the Senior Pool who possess at least 10,000 FIDU tokens or staked FIDU tokens, representing approximately a $10,000 investment to ensure that the LP’s accessing this proprietary data have adequately aligned incentives to protect a Borrower’s best interests.

{% hint style="info" %}
**Note:** The rationale for a $10,000 minimum to participate as a Senior Pool LP is driven by the need to ensure Senior Pool Investors meet an adequately high bar for “skin in the game.” The incredibly sensitive nature of the underlying data Borrowers are reporting can essentially be thought of as trade secrets, given the depth of detail and private company data the Borrowers are reporting in these channels. With Borrowers forming a core component of the Goldfinch protocol, it’s imperative that their interests are protected so that bad actors cannot easily the Borrowers’ sensitive data.
{% endhint %}

The token-gating configuration is executed using the [collab.land](http://collab.land) tool to grant access only to Backers and Senior Pool LPs as described above.&#x20;

The primary purpose of this channel is to facilitate asynchronous communication between Borrowers and Investors. These communications can take a number of forms, including:

* Borrowers informing the capital providers that an update has been made to the Pool’s Dataroom&#x20;
* Borrowers answering questions posted by the Investors in the channel&#x20;
* Borrowers confirming to Investors that an interest payment has been made

### Channel #2: password-gated Dataroom

Each Borrower Pool will also launch a password-gated Dataroom where Borrowers can share documents pertinent to the Borrower Pool in question. This will be managed by the **Borrower**.&#x20;

At a minimum, the Dataroom for each pool will contain the following documents:

1. All fully executed legal documents related to the specific pool&#x20;
2. All waivers, amendments, and default notices&#x20;
3. [Covenant](https://www.investopedia.com/terms/c/covenant.asp) compliance certificates&#x20;
4. Quarterly investor updates&#x20;
5. Portfolio level reporting

It is worth noting that the community has defined minimum standards here in place of uniform reporting requirements as the wide and growing variety of borrower types on the protocol would make it difficult to enforce any strignent documentation requirements. In the future as new pools open, Investors can require specific documentation that might not fit every Borrower be provided as needed.&#x20;

The access instructions for the Dataroom will be contained as a pinned message in the token-gated Discord channel for the pool in question. That way, any Backer or LP who accesses the Discord channel using their pool token or FIDU as verification will be able to easily access the Dataroom password as well.

{% hint style="success" %}
For step-by-step instructions on how to access these channels, view "[**Accessing Borrower communication channels**](guides/accessing-borrower-communication-channels.md)**"** in the [Investor How-To](guides/) section of the documentation.&#x20;
{% endhint %}
