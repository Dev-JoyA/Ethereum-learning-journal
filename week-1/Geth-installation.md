# 📖 Day 5: Running My Own Ethereum Node Locally (Sepolia Testnet)

As part of my Web3 studies at [Web3Bridge](https://web3bridge.com), I learned how to set up a local Ethereum node using an **execution client**.

This helped me understand what really happens *under the hood* when building on Ethereum.

---

## 🧰 What I used

- 🖥 **macOS** machine
- ⚙ **Execution client:** Geth (Go Ethereum)
- 🌱 **Testnet:** Sepolia

---

## ⚙️ Installation steps

### ✅ Install Geth using Homebrew
```bash
brew install ethereum
```

# Verify installation
```bash
geth version
```

# Connect to Sepolia testnet
## Sepolia is a developer-friendly Ethereum test network.

### To sync my local node with Sepolia:
```bash
geth --sepolia
```

## 📦 What this command does:

- Starts the Geth execution client
- Connects to Sepolia peers
- Begins syncing the Sepolia blockchain data locally
- Exposes a **JSON-RPC API** (default: `127.0.0.1:8545`)

---

## 🧪 Why this matters

By running my own node, I can:

- Validate transactions and blocks locally
- Send and test transactions via JSON-RPC
- Deploy and interact with smart contracts
- Avoid relying on third-party providers like Infura or Alchemy

This makes learning Ethereum feel *real*, not just theoretical.



