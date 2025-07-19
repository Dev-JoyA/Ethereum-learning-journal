# 📖 Day 3: From Wallet to Block — Understanding the Journey of an Ethereum Transaction

Today I learned what really happens behind the scenes when we send a transaction from our crypto wallet (like MetaMask).

---

## 🔐 What happens step by step:
- The wallet creates a **digital signature** using your private key and the **ECDSA algorithm**
- The signed transaction is hashed (to get its transaction ID)
- It’s sent to an Ethereum node using the **JSON-RPC API**
- If you don’t run your own node, your wallet connects to a remote node (e.g., Infura)

---

## 🧰 At the node:
- The node’s **execution client** checks:
  - Valid nonce
  - Sufficient balance
  - Correct signature
- If valid, it adds the transaction to the **mempool** (queue of pending transactions)
- Nodes share these transactions through the **peer-to-peer (P2P) network**

---

## ⚙️ Running your own node:
To run your own Ethereum node:
- Install an **execution client** (e.g., Geth, Besu)
- The execution client includes the **EVM** that runs smart contract code as EVM bytecode

---

## 🔗 Becoming a validator:
Ethereum uses **Proof of Stake**.  
To become a validator, you need:
- Execution client
- Consensus client (e.g., Lighthouse, Prysm)
- Validator client
- Plus, stake **32 ETH**

---

## 🏗 How blocks get created:
- Every **slot** (12 seconds), the beacon chain randomly picks:
  - One **proposer** to create a block
  - Several **attesters** to check and attest the block
- The proposer selects transactions from the mempool and builds a block
- Attesters verify and sign attestations: “This block is valid”
- Once enough attestations are collected, the block becomes **finalized**

---

## ⚠️ Validator rewards and penalties:
- Staying online and behaving correctly → earn rewards
- Going offline → small penalties
- Malicious actions (like signing conflicting blocks) → get **slashed** (lose part of your staked ETH)
- Staking protects against **Sybil attacks** (makes it costly to create fake validators)

---

For the full article, see 👉 [From Wallet to Block: Understanding the Journey of an Ethereum Transaction](https://medium.com/@joy.gold13/from-wallet-to-block-understanding-the-journey-of-an-ethereum-transaction-78f2b7769245)
