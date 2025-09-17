# CryptoReal Token

A simple ERC-20 token smart contract that automatically mints 1000 tokens to the creator upon deployment.

## Overview

CryptoReal is a basic ERC-20 token implementation built on Solidity 0.8.24. When deployed, it automatically mints 1000 tokens (with 18 decimal places) to the deployer's wallet address.

## Features

- ✅ **ERC-20 Standard Compliance**: Built using OpenZeppelin's battle-tested ERC20 implementation
- ✅ **Automatic Minting**: 1000 tokens are minted to the creator upon contract deployment
- ✅ **Customizable**: Token name and symbol can be set during deployment
- ✅ **Gas Optimized**: Deployed on Arbitrum One for lower transaction fees

## Contract Details

- **Solidity Version**: 0.8.24
- **License**: LGPL-3.0-only
- **Dependencies**: OpenZeppelin Contracts
- **Total Supply**: 1000 tokens (minted to creator)
- **Decimals**: 18

## Smart Contract Code

```solidity
// SPDX-License-Identifier: LGPL-3.0-only

pragma solidity 0.8.24;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract CryptoReal is ERC20 {

    constructor(string memory name_, string memory symbol_) ERC20(name_, symbol_) {
        _mint(msg.sender, 1000 * 1e18);
    }
}
```

## Deployment

### Network

- **Arbitrum One**: Chosen for lower gas fees compared to Ethereum mainnet

### Prerequisites

- MetaMask or compatible wallet
- ETH on Arbitrum One for gas fees
- Remix IDE or compatible development environment

### Deployment Steps

1. **Open Remix IDE**

   - Go to [remix.ethereum.org](https://remix.ethereum.org)
   - Create a new file named `CryptoReal.sol`

2. **Add Dependencies**

   - Install OpenZeppelin contracts via Remix's package manager
   - Or use the import statement as shown in the contract

3. **Compile**

   - Select Solidity version 0.8.24
   - Compile the contract

4. **Deploy**

   - Switch to Arbitrum One network in MetaMask
   - Deploy the contract with your desired token name and symbol
   - Example: `"CryptoReal"` as name and `"CR"` as symbol

5. **Verify Deployment**
   - Check that 1000 tokens are minted to your wallet
   - Verify the token appears in your wallet

## Usage

Once deployed, the CryptoReal token can be used like any standard ERC-20 token:

- **Transfer**: Send tokens to other addresses
- **Balance Check**: View token balance in wallet
- **Trading**: List on DEXs or use in DeFi protocols
- **Integration**: Use in other smart contracts

## Testing

The contract has been tested on Remix IDE and successfully deployed on Arbitrum One. The testing process included:

- ✅ Contract compilation
- ✅ Deployment simulation
- ✅ Token minting verification
- ✅ Transfer functionality testing

## Security Considerations

- The contract uses OpenZeppelin's audited ERC20 implementation
- No additional minting functions beyond the initial 1000 tokens
- Fixed supply ensures no inflation
- Standard ERC20 security practices apply

## License

This project is licensed under the LGPL-3.0-only license.

## Contributing

This is a simple token contract. If you'd like to contribute or suggest improvements, please feel free to open an issue or submit a pull request.

## Support

For questions or support regarding this token contract, please refer to the Ethereum and Arbitrum documentation or OpenZeppelin's ERC20 implementation guide.

---

**Note**: This is a basic ERC-20 token implementation. For production use, consider additional features like:

- Pausable functionality
- Access control
- Burn mechanisms
- Multi-signature requirements
- Time-locked functions
