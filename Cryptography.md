# 📖 Day 4: How Cryptography Powers Cryptocurrency in Ethereum

Today I learned how cryptography secures Ethereum and makes blockchain trustless and decentralized.

---

## 🔐 Key cryptographic concepts in Ethereum:

- **Asymmetric cryptography:** uses a private key (kept secret) and a public key (shared openly)  
- The private key signs transactions; the public key verifies signatures  
- Private keys are large random numbers (~256 bits) written as 64-character hex strings  
- Public keys are derived from private keys using elliptic curve multiplication (secp256k1 curve) — easy one way, impossible to reverse  
- Ethereum addresses are derived by hashing the last 20 bytes of the public key with **Keccak-256**

---

## 🔄 Cryptographic hash functions (Keccak-256):

- Fixed-size output (256 bits) for any input  
- Deterministic: same input → same output  
- Irreversible: can't retrieve input from output  
- Avalanche effect: tiny input changes cause big output changes  
- Collision-resistant: very unlikely two inputs produce the same hash

---

## 🔑 Summary of security:

- Private keys prove ownership (never shared)  
- Public keys verify signatures  
- Hash functions secure data and create addresses  
- Digital signatures authorize transactions without revealing private keys  

---

Cryptography transforms Ethereum into a secure, decentralized, trustless system — where trust is guaranteed by math, not people.

For the full article, see 👉 [How Cryptography Powers Cryptocurrency in Ethereum](https://medium.com/@joy.gold13/how-cryptography-powers-cryptocurrency-in-ethereum-a3d307d1bf63)
