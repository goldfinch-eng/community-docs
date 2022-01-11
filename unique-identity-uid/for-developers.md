---
description: >-
  This page provides technical guidance on how UID works, and how to integrate
  it with your protocol or dApp.
---

# For Developers

{% hint style="warning" %}
UID should be considered **alpha** **software**. It is used for the Goldfinch protocol, and we would love to see other protocols leverage the work we've done, but we cannot guarantee support or maintenance at this time. Use at your own risk. If you have questions or feedback, please contact us! uid@goldfinch.finance. We'd love to hear from you!
{% endhint %}

### Integrating UID in your smart contracts

To integrate UID into your smart contracts, simply check the balance of your user's address to see if they possess the UID token. In Solidity, it would look like this:

```
# This is using OpenZeppelin's ERC1155 preset contracts:
# https://docs.openzeppelin.com/contracts/3.x/api/token/erc1155#IERC1155
import "@openzeppelin/contracts/token/ERC1155/IERC1155.sol";

contract MyContract {
    address UID_CONTRACT = "0xba0439088dc1e75f58e0a7c107627942c15cbb41";
    uint256 public constant ID_VERSION_0 = 0;

    function hasUID(address userAddress) returns (bool) {
        uint256 balance = IERC1155(UID_CONTRACT).balanceOf(userAddress, ID_VERSION_0);
        return balance > 0
    }
}

```

**Note:** UID currently only operates on Ethereum mainnet. The contract itself can be found [here](https://etherscan.io/token/0xba0439088dc1e75f58e0a7c107627942c15cbb41#readProxyContract)

### Integrating UID in your dApp

For your front-ends, you can similarly integrate UID with the following

```
var Web3 = require('web3');
const web3 = new Web3(Web3.givenProvider);
const minimalAbi = [{"inputs": [{"internalType": "address", "name": "account", "type": "address"}, {"internalType": "uint256", "name": "id", "type": "uint256"}], "name": "balanceOf", "outputs": [{"internalType": "uint256","name": "","type": "uint256"}], "stateMutability": "view", "type": "function"}]
const uidAddress = "0xba0439088dc1e75F58e0A7C107627942C15cbb41"
const UID = new web3.eth.Contract(minimalAbi, uidAddress)

async function hasUID(userAddress) {
  const VERSION_0 = 0
  const balance = parseInt(await UID.methods.balanceOf(userAddress, VERSION_0).call())
  return balance > 0
}

```

### Getting new users verified

If your users don't already have a UID, you can send them to our front-ends to be verified at [app.goldfinch.finance/verify](https://app.goldfinch.finance/verify).

{% hint style="info" %}
**Please note**: UID is only open to non-U.S. individuals right now.&#x20;
{% endhint %}

### **How It Works**

UID is very simple. It works by having a trusted signer (Goldfinch in this case) verify that a given address has passed KYC, and once verified, gives that user a signed message, which they can present to the UID contract in order to mint their UID.

**So the user flow looks like this...**

1. User completes KYC flow (on [app.goldfinch.finance/verify](https://app.goldfinch.finance/verify), via our partner [Persona](https://withpersona.com)).
2. Submit completed KYC to the Trusted Signer, which returns a signed message to the user.
3. User mints their UID by presenting the signed message to the UID contract.

### Security and Privacy

All personal data is processed and handled through [Persona](https://withpersona.com). Persona has industry leading [security and privacy practices](https://withpersona.com/security). **No personal information is stored on-chain.**

### Need to get in touch?

Have questions about integrating? Do you have a certain use case, or feature you'd like to see? The community would love to hear from you. Reach out at **uid@goldfinch.finance**
