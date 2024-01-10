
# **Omnichain Staking Contract**

This repository contains a Solidity smart contract designed for omnichain staking, enabling users to stake tokens across multiple blockchains using ZetaChain technology.

## **Overview**

The **`Staking.sol`** contract provides functionalities for:

- **Staking Tokens**: Users can stake ZRC-20 tokens by depositing them into the contract. Staked tokens accumulate rewards based on the staked amount and duration.
- **Claiming Rewards**: Stakers can claim their accumulated rewards, which are minted to the beneficiary address.
- **Setting Addresses**: Stakers can set their beneficiary address (for reward minting) and a withdraw address (to retrieve staked tokens).
- **Cross-Chain Interaction**: Supports interactions from Ethereum Virtual Machine (EVM)-based chains and Bitcoin testnet. Handles incoming actions from different chains, validating the chain ID and executing respective functions.
- **Gas Fee Handling**: Deducts a gas fee during the unstaking process and withdraws the remaining tokens to the specified address.
- **Address Format Conversion**: Converts between Bech32 and hexadecimal address formats for interoperability between Ethereum and Bitcoin addresses.

## **Usage**

To deploy this contract, follow these steps:

1. Deploy the contract on the desired chain (EVM-based chain or Bitcoin testnet) by providing the necessary parameters: name, symbol, chainID, and system contract address.
2. Interact with the contract functions:
    - Stake tokens using the **`stakeZRC`** function.
    - Unstake tokens using the **`unstakeZRC`** function.
    - Set beneficiary and withdraw addresses using the respective functions.
    - Claim accumulated rewards using the **`claimRewards`** function.
3. Ensure cross-chain interaction:
    - Validate incoming messages and execute appropriate actions based on the provided action code and chain ID.

## **Security Considerations**

- Security checks are implemented to prevent unauthorized access and handle potential overflow/underflow conditions.
- Ensure transactions originate from the system contract to prevent unauthorized calls.

## **Dependencies**

- **`@zetachain/protocol-contracts`**: ZetaChain protocol contracts.
- **`@openzeppelin/contracts`**: OpenZeppelin ERC20 implementation.
- **`@zetachain/toolkit`**: ZetaChain toolkit for BytesHelperLib.

## **Contributors**

- [Your Name](link to your profile or contact information)

## **License**

This project is licensed under the MIT License - see the [LICENSE](https://chat.openai.com/c/LICENSE) file for details.