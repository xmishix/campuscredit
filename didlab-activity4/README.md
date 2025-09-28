# DIDLab — ERC-20 DApp

## 📌 Overview
This project is a minimal decentralized application (DApp) that connects to MetaMask and interacts with an ERC-20 token deployed on the **DIDLab Team 03 network**.  

The DApp allows you to:
- Connect MetaMask and switch to the DIDLab Team 03 chain.
- Load an ERC-20 token (name, symbol, decimals).
- Display the connected account’s token balance.
- Transfer tokens to another address.
- Add the token to MetaMask.
- Auto-update balance when transfers occur.

---

## 🌐 Network Configuration
- **Team**: 03  
- **RPC URL**: `https://hh-03.didlab.org`  
- **Chain ID**: `31339`  
- **Currency**: ETH (18 decimals)

---

## 🪙 Token Information
- **Token Name**: Ethereum  
- **Symbol**: ETH  
- **Decimals**: 18  
- **Initial Supply**: 1,000,000  
- **Contract Address**: `0x49fd2be640db2910c2fab69bb8531ab6e76127ff`  

---

## ⚙️ Prerequisites
- Node.js 22.x installed  
- Python 3 (for running a local web server)  
- MetaMask extension installed in your browser  
- Import the faucet private key into MetaMask to use the pre-funded account  

---

## 🚀 How to Run
1. Clone or open this folder.  
2. Start a local server:
   ```python3 -m http.server 8000```
3. Open the DApp in your browser:
  ```http://localhost:8000 ```
4. Steps inside the DApp:
  - Click Connect & Switch Network → approve in MetaMask.
  - Click Load Token → see token name, symbol, decimals, and your balance.
  - To transfer: enter a valid recipient address and an amount, then click Send.
  - Optionally click Add Token to MetaMask to view the token directly in your wallet.

---

## 📸 Screenshots
  - Connection success (account + network).
  - Token loaded (name, symbol, decimals).
  - Balance displayed.
  - Successful transfer log.

<img width="1435" height="735" alt="image" src="https://github.com/user-attachments/assets/207ddcf2-42dd-4adf-b98b-4c49dcf002ba" />
<img width="929" height="690" alt="image" src="https://github.com/user-attachments/assets/22b23b4a-31b8-474a-a39f-08247b5fad46" />

---

## 📝 Notes
  - The token balance is minted to the deployer account. Use the provided faucet private key to import that account into MetaMask.
  - Make sure MetaMask is unlocked and not running in incognito/private mode (extensions are blocked there).
  - If you see "Returned no data (0x)", double-check that the token address is correct and deployed on the DIDLab Team 03 chain.
