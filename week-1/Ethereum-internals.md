# 🔬 Ethereum Internals: EVM, Accounts, Transactions, Gas & Blocks

---

Ethereum is more than just a platform for digital money—it's a decentralized world computer powered by the **Ethereum Virtual Machine (EVM)**. This deep dive explores the five core components that make Ethereum function:

---

## 🔧 The Ethereum Virtual Machine (EVM)

- The **EVM** is a global computation engine that runs smart contracts.
- It's **stack-based**, allowing up to **1,024 items**, each **256 bits**, aligning with Ethereum’s cryptography standards.
- Types of memory:
  - **Stack:** Short-term, for quick calculations.
  - **Memory:** Temporary storage per transaction.
  - **Storage:** Permanent storage tied to a contract.

### 🔡 Bytecode & Opcodes

- Contracts are compiled into EVM **bytecode**.
- Each operation is an **opcode** (e.g., `ADD`, `BALANCE`).

---

## 👤 Ethereum Accounts

There are **two types of accounts**:
1. **Externally Owned Accounts (EOA)** — controlled by private keys.
2. **Contract Accounts** — deployed on-chain with bytecode.

Each account contains:
- `nonce`: Prevents replay attacks.
- `balance`: ETH in wei.
- `codeHash`: Smart contract code hash.
- `storageRoot`: Root of the contract's storage trie.

---

## 🔁 Ethereum Transactions

- A **transaction** is a signed message that triggers state changes.
- Sent **from EOAs** to EOAs or contract addresses.
  
### Components of a Transaction:

| Field       | Purpose                                      |
|-------------|----------------------------------------------|
| `from`      | Sender address (EOA)                         |
| `to`        | Recipient (EOA or contract)                  |
| `value`     | ETH amount in wei                            |
| `data`      | Function call/input for contract             |
| `gasLimit`  | Max gas allowed                              |
| `gasPrice`  | Price per gas unit                           |
| `nonce`     | Unique ID for ordering                       |
| `signature` | Authorization proof                          |

### 🚦 Transaction Types:
- **Type 0:** Legacy, basic gas pricing.
- **Type 1 (EIP-2930):** Adds `accessList`.
- **Type 2 (EIP-1559):** Adds base fee + priority fee.

---

## ⛽ Gas: Ethereum's Fuel

- **Gas** measures computation effort.
- Prevents spam, infinite loops, and rewards validators.

### EIP-1559 Gas Fee Structure:

| Term         | Definition                                               |
|--------------|----------------------------------------------------------|
| `baseFee`    | Protocol-defined, burned                                 |
| `priorityFee`| Incentive paid to validators                             |
| `maxFee`     | Maximum user is willing to pay                           |

📈 **Cost Formula:** `(BaseFee + PriorityFee) * GasUsed`

---

## ⛓️ Blocks in Ethereum

Blocks organize transactions and secure the chain.

### 📦 Block Contents:

| Part          | Description                                           |
|---------------|-------------------------------------------------------|
| Block Header  | Metadata: slot, proposer, parent hash, state root    |
| Block Body    | Transactions, validator attestations, deposits       |

### ⏱️ Timing & Structure:

- **1 Block every 12 seconds**
- **32 Slots = 1 Epoch = 6.4 minutes**
- **Target block size:** 15M gas
- **Max block size:** 30M gas

### 🧾 Block Lifecycle (Proof of Stake):

1. Validator selected
2. Proposes block with transactions
3. Network attests
4. Finalization after 2/3 attestations

---

## 🧩 How It All Connects

A **user signs a transaction**, which goes to the **mempool**, is picked up by a validator, executed on the **EVM**, and included in a **block**. The network validates and finalizes the block, updating the global state.

---

### 📚 Read the Full Article

👉 [All About Ethereum: Accounts, Transactions, EVM, Gas and Blocks](https://medium.com/@joy.gold13/all-about-ethereum-accounts-transactions-evm-gas-and-blocks-0a75c1fbd0a7)

---