# 🧮 NeekToken Smart Contract

A simple smart contract on Ethereum using Solidity that manages a counter with a description. Only the owner can modify the counter.

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 📦 Contract Overview

**Contract Name:** `NeekToken`  
**Solidity Version:** `^0.8.18`  
**Purpose:** Counter management with access control

---

## 🔧 Features

- ✅ Initialize counter with a custom value and description
- 🔐 Only the contract owner can increment/decrement the counter
- 🔍 Public functions to retrieve counter value and description
- 💸 Gas efficient: View functions cost no gas!

---

## 🛠️ Constructor

```solidity
constructor(uint initial_value, string memory description)
```

- Initializes the counter with:

-  `initial_value`: Starting number

- `description`: Description of the counter

- Sets the contract deployer as the owner

## 👤 Access Control

```solidity
modifier onlyOwner()
``` 

Restricts access to specific functions so only the owner can execute them.

## 🚀 Public Functions
| Function                  | Type                | Description                      |
|---------------------------|---------------------|----------------------------------|
| `increment_counter()`     | External, OnlyOwner | Increases counter by 1           |
| `decrement_counter()`     | External, OnlyOwner | Decreases counter by 1           |
| `get_counter_value()`     | External, View      | Returns current counter value    |
| `get_string_description()`| External, View      | Returns counter description      |


## 🛡️ Security

- All mutation functions are restricted to the `owner` using `onlyOwner` modifier.

- View functions are safe and free to call.