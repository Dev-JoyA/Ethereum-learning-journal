# 📖 Day 7: Ethereum Transactions, Gas, Signatures & Contract Deployment

Today I studied how Ethereum transactions work under the hood: from gas fees and cryptographic signatures to deploying and calling contracts.

---

## 🧠 What I learned:

- Transactions pay fees: `total_cost = gas × gasPrice`
- Gas price often shown in Gwei; `1 Gwei = 10^9 wei`
- Transactions are signed using **ECDSA** → produces `v, r, s`
- Private key **signs** the transaction; it never encrypts or gets shared
- Three tx types:
  | Type | Since | Feature |
  |--|--|--|
  | 0 | Legacy | simple `gasPrice` |
  | 1 | Access List | adds `accessList` |
  | 2 | Dynamic Fee (EIP-1559) | uses `maxFeePerGas` & `maxPriorityFeePerGas` |
- Contract deployment: `to` is empty; `data` has bytecode
- New contract address = `keccak256(rlp.encode([sender, nonce]))`
- Transaction data itself isn’t encrypted; everything on chain is public

---

## ✍️ Full article / detailed notes:
> 📚 [Medium – Ethereum & Blockchain — Study Notes (Today)](https://medium.com/@joy.gold13)


