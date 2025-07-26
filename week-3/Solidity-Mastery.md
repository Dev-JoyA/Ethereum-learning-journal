# 📘 Solidity Concepts Mastery — July 26

This PR adds comprehensive notes and code examples summarizing key foundational Solidity & Web3 concepts. The goal is to solidify understanding of smart contract design patterns and dApp architecture.

---

## ✅ What’s Included

### 🔁 1. Libraries in Solidity
- Modular, reusable logic (like utility/helper functions).
- Internal functions only — no state storage or Ether acceptance.
- Can be attached to types using `using Library for Type`.

### 📡 2. Events, Emit & Indexed
- **Events** act as communication bridges to off-chain systems.
- **`emit`** triggers the logs for frontend or subgraph listeners.
- **`indexed`** allows filtering event logs by up to 3 fields.

### 🧠 3. Data Locations
| Location   | Type       | Editable | Use Case |
|------------|------------|----------|----------|
| `storage`  | Persistent | ✅        | State variables |
| `memory`   | Temporary  | ✅        | Function logic |
| `calldata` | Temporary  | ❌        | External inputs |

### 🏭 4. Factory Pattern
- Contract that **deploys** multiple instances of another contract.
- Common in wallets, games, DAO templates.

### 🕸️ 5. The Graph
- Decentralized protocol for indexing blockchain data.
- Listens for contract **events** and structures them for **GraphQL** queries.

### 🌐 6. Blockchain Explorers
- Sites like **Etherscan**, **Celoscan**, used to view:
  - Transactions
  - Contract source code
  - Emitted events and internal calls

---

## 🧩 Final Code Integration

```solidity
library ScoreLib {
    function boost(uint x) internal pure returns (uint) {
        return x + 10;
    }
}

contract Game {
    using ScoreLib for uint;

    event ScoreUpdated(address indexed player, uint newScore);

    mapping(address => uint) public scores;

    function play() public {
        scores[msg.sender] = scores[msg.sender].boost();
        emit ScoreUpdated(msg.sender, scores[msg.sender]);
    }
}
