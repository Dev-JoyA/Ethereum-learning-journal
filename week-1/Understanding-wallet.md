# 📖 Day 2: Understanding Wallet in Ethereum

Today I learned what a **wallet** really means in Ethereum.

- Unlike a physical wallet, an Ethereum wallet is a **software application** that helps us:
  - Manage our Ethereum account
  - Store and use our private key securely
  - Send and receive Ether (ETH)

The smallest unit of Ether is called **wei**.

---

## 🧰 Types of wallets
- Web wallets, mobile wallets (iOS/Android), desktop wallets
- Choose based on security, ease of use, and platform
- Example: **MetaMask** (browser extension)

During setup, wallets give you a **secret recovery phrase** (seed phrase).  
🔑 This phrase is private and used to generate your private key — keep it safe!

---

## 🔑 Externally Owned Account (EOA)
- Controlled by a private key that the user holds
- Popular wallets like MetaMask create EOAs
- With EOAs you can:
  - Create multiple accounts
  - Send/receive ETH
  - Interact with smart contracts
  - Switch between mainnet and testnets (Sepolia, Linea Sepolia, Mega Testnet)
- Transactions can be viewed on blockchain explorers like [Etherscan](https://etherscan.io/)

---

## 📦 Contract Account
- Created by deploying smart contracts to the Ethereum network
- Doesn’t have a private key → can’t initiate transactions
- Triggered when they receive transactions from EOAs or other contracts
- Can store data, execute code, and interact with other contracts
- Have their own Ethereum address

Smart contracts make Ethereum programmable and power dApps, DeFi, NFTs, etc.

---

For the full article, see 👉 [Understanding Wallet in Ethereum](https://medium.com/@joy.gold13/understanding-wallet-in-ethereum-1ccc6bfe1f40)
