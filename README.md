# 🪙 MyToken (MTK) - ERC-20 Smart Contract
# 📌 About This Project
Welcome to MyToken, a fully functional cryptocurrency token I built on the Ethereum blockchain. This project represents my "Hello World" into Web3 development, designed to understand the fundamental architecture of decentralized assets.

I developed this smart contract using Solidity and the ERC-20 standard, ensuring it functions exactly like major tokens (such as USDT or LINK) regarding transfers, balance tracking, and approval mechanisms.

# ⚙️ Technical Specifications
Token Name: MyToken

Symbol: MTK

Decimals: 18 (Standard Ethereum precision)

Total Supply: 1,000,000 MTK

Contract Address: (Deployed on Remix VM)

# 🚀 Features I Implemented
To ensure full compliance with the ERC-20 standard, I implemented the following core functions:

transfer: Logic to securely move tokens from the caller's wallet to another address.

approve & transferFrom: A two-step process allowing third-party decentralized applications (DApps) to spend tokens on my behalf—a critical feature for DeFi protocols.

balanceOf: A view function to query the token holding of any specific wallet.

allowance: Tracks how many tokens a spender is still authorized to use.

Event Logging: I utilized emit Transfer and emit Approval to ensure all state changes are logged on the blockchain for transparency.

Error Handling: Integrated require statements to prevent invalid transactions (e.g., sending to a zero address or exceeding balance).

# 🛠️ Tech Stack
Language: Solidity (Version 0.8.26)

IDE: Remix (Browser-based Ethereum IDE)

Testing Environment: Remix VM (Cancun)

# 💻 How I Deployed It
Environment Setup: I used Remix IDE to handle compilation and local deployment.

Compilation: Configured the Solidity Compiler to 0.8.26 to utilize built-in overflow protection.

Deployment:

Selected the Remix VM to simulate the Ethereum blockchain.

Passed the initial supply calculation to the constructor: 1000 * 10^18.

Successfully deployed and verified the contract instance.

# 📖 Usage Guide
Here is how to interact with the contract once deployed:

*** `1. Transferring Tokens`**
To send tokens to a peer:

Solidity

// Call the transfer function
transfer(0xRecipientAddress..., 1000000000000000000); 

*** `2. Checking Balances`**
To see how many tokens an address holds:

Solidity

// Call balanceOf
balanceOf(0xYourAddress...);

*** `3. Approving a Spender`**
To authorize a DApp or another user to spend tokens:

Solidity

// Call approve
approve(0xSpenderAddress..., 5000000000000000000); 
# 🧠 What I Learned
Building this project gave me hands-on experience with several key blockchain concepts:

State Management: How mapping(address => uint256) is used efficiently to replace traditional database ledgers.

Atomic Transactions: Understanding that if one requirement fails (e.g., insufficient balance), the entire transaction reverts to ensure safety.

Events & Logs: Why emitting events is crucial for frontend applications to "listen" to blockchain activity.

Decimal Precision: I learned that Solidity does not support floating-point numbers, requiring the use of 18 decimal places for calculations.

# 📄 License
This project is open-source and available under the MIT License.
