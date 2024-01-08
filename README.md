# **Staking Contract on ZetaChain**

This Solidity smart contract implements a staking mechanism allowing users to stake ERC20 tokens, earn rewards based on staked amounts and time, and claim accumulated rewards. The contract is designed to operate within the ZetaChain ecosystem.

## **Overview**

The **`Staking`** contract inherits from **`ERC20`** and **`zContract`**, providing functionality for staking, tracking stake amounts, managing rewards, and enabling the claiming of rewards.

### **Features**

- **Staking Functionality**: Users can stake ERC20 tokens into the contract.
- **Reward Calculation**: Rewards are calculated based on staked amounts and time duration.
- **Reward Claiming**: Stakers can claim their accumulated rewards.

## **Contract Structure**

### **Prerequisites**

- Solidity ^0.8.7
- Dependencies:
    - **`@zetachain/protocol-contracts`**
    - **`@openzeppelin/contracts`**
    - **`@zetachain/toolkit`**

### **Contract Functions**

- **`stakeZRC`**: Allows users to stake ERC20 tokens.
- **`unstakeZRC`**: Enables users to withdraw their staked tokens.
- **`setBeneficiary`**: Sets the beneficiary address for rewards.
- **`claimRewards`**: Allows stakers to claim their accumulated rewards.

## **Usage**

### **Deployment**

To deploy this contract:

1. Provide the required parameters: **`name_`**, **`symbol_`**, **`chainID_`**, and **`systemContractAddress`**.

### **Interacting with the Contract**

- **Staking**: Use the **`stakeZRC`** function to stake tokens.
- **Unstaking**: Tokens can be withdrawn using the **`unstakeZRC`** function.
- **Setting Beneficiary**: Use the **`setBeneficiary`** function to set the beneficiary address for rewards.
- **Claiming Rewards**: Stakers can claim their rewards using the **`claimRewards`** function.

## **Development**

### **Setting Up Development Environment**

1. Clone the repository.
2. Install dependencies using Node.js and Yarn:
    
    ```bash
    yarn install
    ```
    
3. Develop and test the contract on the ZetaChain testnets or local development environments.

## **Contributions**

Contributions and improvements are welcomed! Fork the repository, make necessary changes, and submit a pull request.

## **License**

This project is licensed under the MIT License. See the LICENSE file for details.
