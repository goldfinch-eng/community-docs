---
description: Below are some key mechanics of a debt facility on the Goldfinch Protocol
---

# Debt Facility Mechanics

### **Revolving Credit Facility**

**Borrower Pools on the Goldfinch protocol work like a revolving credit facility**. Borrowers have the ability to withdraw and repay (as many times as they like) any amount provided the total outstanding amount at any time is less than the Borrower Pool's credit limit. There are no prepayment penalties.\
\
However, it is worth noting that any amount of capital left unutilized in a Borrower Pool can be withdrawn by Backers at any time. This means that although the protocol offers a revolving credit facility, it is not a committed facility. It is designed this way to give Backers liquidity, and to ensure that borrowers do not pay fees on unused capital)

### Facility Tranches

Each borrower pool has the ability to accommodate multiple tranches of the same facility. This allows borrowers to grow the size of capital they draw from the protocol without having to launch new Borrower pools.

### **Interest Payments**

The Goldfinch protocol is built to expect interest payments to be made every thirty days, starting from the day a Borrower draws down funds into their wallet. Interest is calculated on an Actual / 365 basis

### Facility and Security Agents

As no centralized party provides any administrative roles for transactions on the Goldfinch protocol, Borrowers need to externally source and bear the cost of any facility/admin/security agents required in agreements.\
