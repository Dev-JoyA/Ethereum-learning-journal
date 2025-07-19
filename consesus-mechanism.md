# Understanding Consensus in Ethereum: From Proof of Work to Proof of Stake

Consensus mechanisms power the trust and coordination behind decentralized networks like Ethereum. This post breaks down how Ethereum transitioned from **Proof of Work (PoW)** to **Proof of Stake (PoS)** — and what that means for security, efficiency, and decentralization.

---

## 🔁 What Is Consensus?

It’s how thousands of nodes agree on the state of the blockchain — ensuring no double-spending, maintaining data integrity, and preserving decentralization.

---

## 🔨 Ethereum’s Shift: PoW ➝ PoS

- **PoW** (Before 2022): Miners solved puzzles to add blocks — energy-heavy, prone to centralization.
- **PoS** (After Merge): Validators stake ETH to propose and attest blocks — greener, faster, more secure.

---

## 🔍 Core PoS Concepts

| Term         | What It Means                                               |
|--------------|-------------------------------------------------------------|
| **Slot**     | 12s window to propose a block                               |
| **Epoch**    | Group of 32 slots (6.4 mins)                                |
| **Checkpoint** | 1 per epoch, used for finality                            |
| **Finality** | Block is irreversible after 2/3 validator attestation       |
| **Attestation** | Validator votes “yes” on a proposed block               |
| **LMD-GHOST** | Picks chain with most validator weight behind it           |

---

## ✅ Finality & Security

- Validators propose + attest blocks.
- Every **32 slots**, a **checkpoint** is proposed.
- If 2/3 of staked ETH supports it → it's **justified**, and if the next one is also justified → the previous is **finalized**.
- Finalized blocks can’t be reversed without **slashing** malicious validators.

---

## ⚔️ Rewards & Penalties

- **Earn:** Proposing blocks, attesting, and sync committee duties.
- **Lose:** Being offline, double-signing, or voting inconsistently.
- **Slashing** = severe penalty for breaking the rules.

---

## 🔐 Validator Keys

- **Signing Key:** Must stay online to sign blocks and attestations.
- **Withdrawal Key:** Used to withdraw staked ETH (can be stored offline).

---

## Why It Matters

Ethereum’s PoS system brings:
- **Sustainability** (no mining energy waste)
- **Security** (economic penalties enforce good behavior)
- **Scalability** (more efficient block production)


