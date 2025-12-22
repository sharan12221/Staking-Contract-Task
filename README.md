# 🏦 Staking Smart Contract

A secure and gas-efficient staking smart contract that enables users to stake ERC-20 tokens (USDT-compatible) and earn rewards at a fixed **10% APY**, with support for **automatic rollover (compounding)** and **independent reward claims**.

---

## ✨ Key Features

* **Fixed 10% APY**
  Predictable and transparent reward model.

* **30-Day Lock Period**
  Funds are locked for a fixed duration to ensure staking stability.

* **Automatic Rollover (Compounding)**
  Users can roll over stakes to compound rewards **without incurring tax**.

* **Independent Reward Claims**
  Claim rewards without unstaking the principal.

* **Withdrawal Tax Mechanism**
  A **0.5% tax** applied on unstake and reward claims, routed to a treasury.

* **Multiple Concurrent Stakes**
  Each user can create and manage multiple active stakes.

* **Security-First Design**
  Built with OpenZeppelin contracts, including:

  * Reentrancy protection
  * Pausability
  * Safe ERC-20 handling

---

## 🚀 Getting Started

### Prerequisites

* Node.js **v20+**
* npm
* Hardhat

---

### Installation

```bash
# Clone the repository
git clone https://github.com/sharan12221/Staking-Contract-Task.git
cd Staking-Contract-Task

# Install dependencies
npm install
```

---

### Environment Configuration

Create a `.env` file from the example:

```bash
cp .env.example .env
```

Update `.env` with your values:

```env
PRIVATE_KEY=your_private_key_here
SEPOLIA_RPC_URL=https://sepolia.infura.io/v3/YOUR_INFURA_KEY
GOERLI_RPC_URL=https://goerli.infura.io/v3/YOUR_INFURA_KEY
ETHERSCAN_API_KEY=your_etherscan_api_key
STAKING_TOKEN_ADDRESS=0x...   # USDT or ERC20 token address
TREASURY_ADDRESS=0x...        # Treasury wallet address
```

---

## 🧪 Testing

Run the full test suite:

```bash
npx hardhat test test/test.js
```

Tests cover:

* Staking and unstaking flows
* Reward calculation accuracy
* Tax deductions
* Rollover logic
* Edge cases and access control

---

## 📦 Deployment

### Deploy to Sepolia

```bash
npx hardhat run scripts/deploy.js --network sepolia
```
