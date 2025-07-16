# 📖 Day 8: EIP Core Concepts – Gas, REVERT, and Smart Contract Memory

Today I explored some core Ethereum Improvement Proposals (EIPs) that enhance the way smart contracts manage **gas**, **errors**, and **return values**. Specifically: `EIP-5` and `EIP-140`.

---

## ✅ EIP-5: Gas Usage for `RETURN` and `CALL*`

**Purpose**: Improve gas efficiency when returning data of unknown length.

### 🔹 Before EIP-5:
- Contracts pay gas for the **entire reserved memory**, regardless of how much is actually returned.

### 🔹 After EIP-5:
- You only pay for **memory actually written to**.
- This is crucial for:
  - Proxy contracts
  - Dynamic return values (e.g. arrays, strings)
  - Unknown-length responses

✅ Result: More efficient, flexible, and safe smart contract design.

---

## ✅ EIP-140: The `REVERT` Instruction

**Purpose**: Abort contract execution, rollback changes, and return a readable error message — all without consuming all remaining gas.

### 🔹 New Opcode Introduced:
- `REVERT (0xfd)`
- Syntax: `REVERT(memory_offset, memory_length)`

### 🔹 Benefits:
- Returns **custom error messages**
- Saves unused gas
- Enables better debugging and safer failure handling

### 🔹 In Solidity:
```solidity
require(condition, "Error message");
revert("Custom error");
