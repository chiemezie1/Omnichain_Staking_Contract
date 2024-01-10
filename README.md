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

### **Step 1: Setting Up Development Environment**

1. Clone the repository.
2. Install dependencies using Node.js and Yarn:
    
    ```bash
    yarn install
    ```
    
### **Step 2: Creating and Funding Wallet**

1. **Wallet Creation**: Run **`npx hardhat account --save`** in your terminal to generate a new wallet. The command will create the wallet and generate a **`.env`** file with private key details.
2. **Funding with Testnet Tokens**:
    - Acquire ZETA tokens using **`npx hardhat faucet`**.
    - Get MATIC tokens from the Polygon Mumbai Faucet.
    - Obtain BTC tokens from a Bitcoin testnet faucet using your Bitcoin address.
3. **Check Wallet Balances**: Verify the token balances using **`npx hardhat balances`** to ensure successful funding.


### **Step 3: Function Action Codes Recap**

```
const data = prepareData(args.contract, ["uint8"], ["1"]); // Staking tokens

```

### **Step 4: Interacting with EVM-based Chain (e.g., Polygon Mumbai Testnet)**

1. **Deploy Contract**: Execute **`npx hardhat compile --force`** followed by **`npx hardhat deploy --network zeta_testnet --chain mumbai_testnet`**.
2. **Setting Beneficiary Address**:
    - Use **`npx hardhat set-beneficiary <ACCOUNT_ADDRESS> --contract <CONTRACT_ADDRESS> --network mumbai_testnet`**.
3. **Setting Withdraw Address**:
    - Execute **`npx hardhat set-withdraw --contract <CONTRACT_ADDRESS> --network mumbai_testnet`**.
4. **Staking Tokens**:
    - Stake tokens via **`npx hardhat stake --amount 0.1 --contract <CONTRACT_ADDRESS> --network mumbai_testnet`**.
5. **Unstaking Tokens**:
    - Unstake tokens using **`npx hardhat unstake --contract <CONTRACT_ADDRESS> --network mumbai_testnet`**.

### **Step 5: Interacting with Bitcoin Testnet**

1. **Deploy Contract to Bitcoin Testnet**:
    - Deploy the contract to the Bitcoin testnet using **`npx hardhat deploy --network zeta_testnet --chain btc_testnet`**.
2. **Set Beneficiary and Withdraw Addresses**:
    - Set addresses for beneficiary and withdraw using Bitcoin transactions.
3. **Stake and Unstake BTC Tokens**:
    - Stake and unstake BTC tokens via Bitcoin testnet transactions.


## **Contributions**

Contributions and improvements are welcomed! Fork the repository, make necessary changes, and submit a pull request.

## **License**

This project is licensed under the MIT License. See the LICENSE file for details.