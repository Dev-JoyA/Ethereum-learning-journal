# 📚 Day 11: Web3 & Blockchain Concepts — Complete Summary

Today I covered fundamental Web3 concepts and how decentralized applications (dApps) work under the hood.

---

## 1. Web Evolution

- **Web1:** Static, read-only websites.
- **Web2:** Interactive, centralized apps with user data controlled by Big Tech.
- **Web3:** Decentralized apps (dApps), users own data & interact trustlessly via smart contracts.

---

## 2. Key Web3 Components

- **DAOs:** Decentralized Autonomous Organizations governed by token holders.
- **Ownership:** Shift from centralized control to community governance.
- **API vs ABI:** API connects apps; ABI defines smart contract interfaces for frontend interaction.

---

## 3. Frontend & Blockchain Interaction

- **Provider:** Connects frontend to blockchain node (read-only).
- **Signer:** User wallet that signs transactions (write).
- Use `ethers.Contract(address, abi, signer)` to call smart contracts.

---

## 4. RPC API & Wallets

- dApps send JSON-RPC calls to nodes (Infura, Alchemy).
- Wallets (MetaMask, Trust Wallet) manage private keys.
- WalletConnect bridges mobile wallets.

---

## 5. Chains & Chain IDs

- Unique IDs identify blockchains and prevent replay attacks.
- Different chains: Ethereum, Polygon, BSC.

---

## 6. Other Concepts

- **Chainlink:** Oracle network for real-world data.
- **Lisk:** Independent blockchain with JavaScript SDK.
- Wallet balances show ETH + USD value; fees shown in Gwei.

---

## 7. Events & Data Indexing

- Solidity **events** log data on-chain; frontends listen to update UI.
- **The Graph** indexes blockchain data for efficient querying.
- IPFS and Swarm provide decentralized storage for large files.

---

## 8. Ethereum Provider Standards

- **EIP-1193:** Standardizes `window.ethereum` API.
- **EIP-6963:** Allows detecting multiple wallets.

---

## 9. Handling Missing Wallets

- Notify users to install wallets if `window.ethereum` is null.
- Use public RPC for read-only access.

---

## 10. Provider vs Signer Summary

| Component | Role                             |
| --------- | --------------------------------|
| Provider  | Reads blockchain data            |
| Signer    | Signs transactions for blockchain writes |

---

## 11. Web3 dApp Architecture

User Frontend (React + ethers.js)  
↓  
Provider (MetaMask, WalletConnect, Infura)  
↓  
Blockchain Node (RPC API)  
↓  
Ethereum Virtual Machine (EVM)  
↓  
Events & Contract State → Frontend listens  
↓  
IPFS / Swarm stores files, blockchain stores hashes
