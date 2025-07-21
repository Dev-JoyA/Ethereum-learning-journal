# 📘 Day 10: Ethereum Blockchain Development — Core Concepts Summary

Today I focused on understanding the full lifecycle of Ethereum decentralized application (DApp) development — from writing smart contracts to how they run on the Ethereum Virtual Machine (EVM).

---

## 🧱 1. DApp Development

- A DApp has:
  - **Frontend**: HTML, JavaScript, React, etc.
  - **Backend**: Smart contracts (Solidity)
  - **Web3 connection**: via Ethers.js or Web3.js
  - **Optional Storage**: IPFS or Filecoin

🛠 Example: A marketplace where smart contracts handle listings and purchases.

---

## 🛠 2. Development Environment Setup

| Tool     | Use Case                    |
|----------|-----------------------------|
| Remix    | Simple, in-browser IDE      |
| Hardhat  | Advanced local dev + testing |
| Truffle  | Testing & deployment        |
| Foundry  | Fastest execution, CLI-based |
| Ganache  | Local blockchain simulator  |

💡 Sepolia testnet lets you practice without real ETH.

---

## 🧮 3. Opcodes & EVM Stack

- EVM executes low-level **opcodes** like `ADD`, `PUSH`, `SSTORE`.
- Every smart contract is compiled into these opcodes.
- Stack: Holds up to **1024 items**, each **256 bits**.
- Each opcode costs **gas** (i.e., ETH fee for computation).

---

## 📚 4. Ethereum Development Stack

- EVM (runtime)
- Solidity (language)
- Hardhat / Foundry (frameworks)
- Ethers.js / Web3.js (communication)
- IPFS / Filecoin (optional storage)

Choose based on complexity:
- 🔰 Beginner: Remix + Sepolia
- 🧠 Pro: Hardhat + Ethers.js

---

## 🆔 5. Account Types & Differences

| Type        | Control        | Created By          |
|-------------|----------------|---------------------|
| EOA         | Private Key    | Wallet (e.g., MetaMask) |
| Contract    | Smart Contract | Deployment by user  |

- Contract Account = code + data + ETH
- Smart Contract = the actual code logic

---

## 🧠 6. Solidity Memory Models

| Term      | Description                               |
|-----------|-------------------------------------------|
| Storage   | Permanent, costly, saved to blockchain    |
| Memory    | Temporary, per function call              |
| Stack     | Very fast, limited, for computation       |
| Calldata  | Read-only input arguments to functions    |

---

## 🔐 7. Function Types

### Behavior:
- `pure`: No blockchain read/write
- `view`: Reads state
- `payable`: Accepts ETH

### Visibility:
- `public`, `external`, `internal`, `private`

---

## 🛠 8. Libraries vs Frameworks

| Type      | Purpose                          |
|-----------|----------------------------------|
| Library   | Utility code (e.g., OpenZeppelin) |
| Framework | Full lifecycle (e.g., Hardhat)    |

---

## 🧵 9. Solidity to EVM Flow

```text
Solidity Source → Compiler (solc) → Bytecode → Opcodes → EVM Executes
