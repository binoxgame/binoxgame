# 🎮 Binox Game

**Binox Game** is a blockchain-powered numbers game built on **BNB Smart
Chain (BSC)** where users can place bets, win rewards, and interact with
a decentralized payment system.

The platform integrates **BNB payments**, smart contracts, and a
**React-based frontend** to provide a fast and transparent gaming
experience.

🌐 Website: https://binoxgame.fun

------------------------------------------------------------------------

# 🚀 Technology Stack

-   **Blockchain**: BNB Smart Chain (BSC)
-   **Smart Contracts**: Solidity \^0.8.20
-   **Frontend**: React.js
-   **Web3 Integration**: ethers.js
-   **Oracle**: Chainlink BNB/USD Price Feed
-   **Development Framework**: Hardhat / OpenZeppelin

------------------------------------------------------------------------

# 🌐 Supported Networks

  Network                       Chain ID
  ----------------------------- ----------
  **BNB Smart Chain Mainnet**   56
  **BNB Smart Chain Testnet**   97

------------------------------------------------------------------------

# 📜 Contract Addresses

  Network           Contract
  ----------------- ----------------------------------------------
  **BNB Mainnet**   `0xac1344FdeC20De2B624B1D170b1169c8b4ccD903`

------------------------------------------------------------------------

# ⚡ Core Features

### 🎮 Blockchain Numbers Game

Players can select numbers and place bets through the web interface.

### 💰 BNB Payment Gateway

Users can fund their game balance using **BNB payments** verified by the
smart contract.

### 📊 Real-Time BNB Price Conversion

The contract uses **Chainlink Price Feed** to convert BNB value into
USD.

### 🔒 Secure Smart Contract

The contract includes:

-   Owner controlled payments
-   Price validation using Chainlink
-   Minimum and maximum USD limits
-   Secure payment forwarding

### ⚡ Fast Transactions

Powered by **BNB Smart Chain**, ensuring:

-   Low gas fees
-   Fast confirmations
-   High scalability

------------------------------------------------------------------------

# 💳 Payment Limits

The payment gateway enforces the following limits:

  Limit             Value
  ----------------- -------
  Minimum Payment   \$1
  Maximum Payment   \$50

------------------------------------------------------------------------

# 📄 Smart Contract Overview

### Contract Name

`BNBPaymentGate`

The contract handles **BNB payments for game transactions** and converts
them to USD value using Chainlink.

------------------------------------------------------------------------

### Pay with BNB

``` solidity
function pay(
    string calldata userId,
    string calldata orderId
) external payable
```

Users send BNB along with their **user ID and order ID** to process game
payments.

------------------------------------------------------------------------

### Get BNB/USD Price

``` solidity
function getBNBUsdPrice() public view returns (uint256)
```

Fetches the **latest BNB price from Chainlink Oracle**.

------------------------------------------------------------------------

### Convert BNB to USD

``` solidity
function getBNBUsdValue(uint256 bnbAmount) public view returns (uint256)
```

Returns the USD value of BNB sent.

------------------------------------------------------------------------

# 🔔 Payment Event

Every successful payment emits an event:

``` solidity
event PaymentReceived(
    address indexed payer,
    string userId,
    string orderId,
    uint256 bnbAmount,
    uint256 usdValue
);
```

This allows the frontend to track **user deposits and game activity**.

------------------------------------------------------------------------

# 🔐 Security

Security features include:

-   Chainlink price oracle
-   Minimum & maximum payment limits
-   Owner-controlled withdrawal
-   Safe transfer mechanisms

------------------------------------------------------------------------

# 🛠 Development Setup

### Install Dependencies

``` bash
npm install
```

### Run Frontend

``` bash
npm start
```

### Deploy Contracts

Using **Hardhat**

``` bash
npx hardhat compile
npx hardhat deploy
```

------------------------------------------------------------------------

# 📈 Future Roadmap

Planned improvements for Binox Game:

-   🎯 On-chain random number generator
-   🎮 More game modes
-   💎 Token rewards integration
-   📊 Leaderboard system
-   🌐 Multi-chain support

------------------------------------------------------------------------

# 📜 License

MIT License
