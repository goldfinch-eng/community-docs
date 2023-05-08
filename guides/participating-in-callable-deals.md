---
description: >-
  Callable loans provide Backers with the flexibility to call back their capital
  with 2 months notice.
---

# Participating in Callable Deals

Backers evaluate Callable Deals and provide capital to a single tranche of the deal itself. This new deal went live in March 2023, after community and governance approved the new pool type.

## **Learning about a Callable Deal**

**How Callable Deals work**

Callable loans are an existing structure in traditional finance that provides liquidity to investors by giving them the right to “call back” their capital at regular intervals.

On Goldfinch, the Callable Deal loan structure gives Backers the right to “call back” their invested capital. Borrowers are required to return 100% of this “called capital” at the end of a “call period.”

For the initial design, call periods will occur every three months and call requests must be submitted **at minimum 2 months** before the end of the call period (any calls that occur less than 2 months before the closest upcoming repayment date will be paid on the second closest upcoming repayment date).

**Example Callable Deal**

Callable loans are a suitable option for borrowers with short-term assets that can be liquidated when investors want to redeem their capital. Callable loans are used in traditional finance, but their structure and terms are usually customized to match the capital structure of the Borrower.

As an example deal:

* Borrower: Fintech X, who provides buy-now-pay-later (BNPL) loans to customers with a maximum tenor of 30 days
* Goldfinch Deal Terms: 2 year loan with a quarterly call period where Backers must serve their call notice at least 2 months in advance

Fintech X borrows from Goldfinch in order to offer more BNPL loans. If a Backer calls back their position early, Fintech X will know at least 2 months in advance. So they wait to get repaid on their 30 day BNPL loans and use that cash to repay Backers’ called capital.

**Recalling Principal**

As mentioned above, Backers with UID can submit call requests to recall any portion of their principal at any point in time — but must be done at least 2 months in advance to call the next repayment. Once a request is submitted, the Backer continue to receive interest on capital until it is withdrawn.

The illustration below shows a sample deal that demonstrates how the payback period works.

<figure><img src="../.gitbook/assets/Screenshot 2023-05-08 at 4.44.20 PM.png" alt=""><figcaption><p>Call submission scheduling</p></figcaption></figure>

For example: If you submit a call on the earliest possible date in the window (May 1), the time-to-repayment is five months; if you submit on the last possible day of the period (July 31), the time-to-repayment is two months. If a borrower is late on any payments, the ability to submit call requests will remain active.

**Understanding the risks**

**It is important to understand that you can lose money by participating in Callable Deals.** If a Borrower doesn't repay the amount they borrow, you will lose your relative portion of that amount. The Borrower repayments are applied pro-rata to outstanding balances in the following order:

1. All existing interest obligations
2. All existing call request principal obligations **which have been locked in,** in order of the call request period they were submitted in.
3. All accrued interest up until now
4. Remaining principal balance

Notes: Since initial Callable loans will be bullet loans, in most cases only (1), (2) & (3) apply; in the case of early principal repayments, the full waterfall applies, including (4). The addition of (2) in the repayment waterfall differs from our current deals.

**When Callable Deals are open**

You can only participate in a Callable Deal when the Callable Deal is open. Otherwise, the dapp will show that the pool is `Full` and you will no longer be able to supply capital. You can look out for announcements to see when new Borrower Pools are going to be open by[https://deals.goldfinch.finance/](https://deals.goldfinch.finance/).

**Announcements**

Typically, once a Callable Deal is open, the community shares announcements using [Discord](https://discord.com/invite/HVeaca3fN8), Twitter, and an email list. Once the deal is live on the dapp, the deal page typically holds the key terms of the loan agreement, a credit memo, a data room, the repayment schedule, FAQs, and other resources.

**Getting more details about Callable Deals**

Usually, the deal page on the dapp includes both a credit memo and a data room with Non-Disclosure Agreements for you to sign. (Read more about NDA's [here](https://www.investopedia.com/terms/n/nda.asp).) This will give you access to the credit memo, produced by third-party professional credit analysts, and the due diligence data room containing information provided by the Borrower.

Each individual Goldfinch Backer is responsible for doing thorough due diligence on their own investments and deciding whether it's a good opportunity for them.

In addition, after you sign the NDA, there is usually a deal-specific Telegram group and/or Discord channel you can join. There, you can ask Borrowers questions directly, both about who they are and the specifics of the deal.

## **Supplying to a Callable Deal**

Each Callable Deal has a unique set of terms and requirements, but all will require a UID to access ([Verify your identity](https://docs.goldfinch.finance/goldfinch/guides/verifying-your-identity) to mint your UID).

1. When the pool is open, visit[https://app.goldfinch.finance/earn](https://app.goldfinch.finance/earn) and click on Callable Deal under the `Open Deals` list. Note: when a Callable Deal is full and closed, it will move to the `Closed Deals` section.
2. On the deal page, click `Supply` to view the form. Review the agreement that is linked to understand what you are signing, enter your full name (this is your signature), and enter the amount of USDC you want to supply. Note: You will be required to enter your full legal name as was provided when registering your UID, and this name will be added to the Borrower's off-chain transaction agreement. This gives you all the associated rights, benefits, and security of the transaction you are investing in. Sometimes, pools will have a cap on the maximum amount that can be supplied. You may need to adjust your investment amount accordingly.
3. Review the terms and click `I Agree`.
4. Approve the transaction in your wallet.
5. Done. You should now see the USDC balance you supplied in your balance at the top of the page. Note: When you supply to a Borrower Pool, you receive an NFT that acts a "digital receipt" representing the amount you supplied. Learn more about this in the [Backer](https://docs.goldfinch.finance/goldfinch/protocol-mechanics/backers) section of the documentation.

## Call Requests

After you supply capital, you can withdraw up until the time when the deal is closed (which typically happens once when the deal is full).

After the Borrower draws down the capital, Backers can submit call requests to recall their principal at any point of time. Repayment of call requests happens once every three months on a set date.

\
**Timing**

Call requests must be received in the first month of the three month call request period (two months prior to a repayment date) in order to be paid. Any calls that occur less than two months before the closest upcoming repayment date will be paid on the second closest upcoming repayment date.\


**How To Submit a Request**

1. Navigate to the deal’s page in the dapp.
2. Click `Submit Call Request`and enter the amount of USDC you want to call back from the deal. Note the expected repayment date.
3. Click `Submit`.
4. `Accept` the transaction in your wallet.

**How to Withdraw Capital**

1. Return to the deal’s page in the dapp on the expected repayment date.
2. Click `Withdraw`
3. Click `Submit`
4. `Accept` the transaction in your wallet.
5. Done. Following network transaction times you should see the USDC you withdrew in your wallet.

## **FAQ**

**What cryptoassets can I supply to Callable Deals?**

Callable deals only support USDC investment.

**When do I receive yield?**

You receive yield each time the Borrower makes an interest payment into the Borrower Pools.

**When do I receive principal?**

You can call any portion of their principal at any point in time — but must be done at least 2 months in advance to call from the next repayment. Once a request is submitted, you will continue to receive interest on capital until it is withdrawn.

**Do I need to sign a Non-Disclosure Agreement (NDA) to invest as a Backer?**

Technically no, but it's strongly recommended that you do sign the NDA in order to review the credit memo and full due diligence materials about the Callable Deals you participate in.

**What happens if I provide a fake name when I supply capital?**

You will forfeit your legal rights to the real-world loan document you are signing. You will still be able to supply capital into the Callable Deals and receive your portion of repayments made on-chain. However, you will have no real-world legal recourse. The Borrower and other Backers will additionally have no obligations to make any repayments to you in the event that there is a a default and they come to a decision regarding how to resolve it.

**Are Backers able to take legal action if Borrowers default?**

Yes, if there is a real-world legal agreement between the Borrower and Backers. When you enter your full name, you are directly signing the agreement with the Borrower that is linked in the form. The process by which a Backer can take action against a Borrower will depend on the specific real-world documents related to the pool a Backer invested in.
