# 🚚 TrustDrive: Blockchain-Powered Supply Chain Management

TrustDrive is a full-stack decentralized application (dApp) designed to bring **transparency**, **trust**, and **tamper-proof tracking** to modern supply chains. By leveraging Ethereum smart contracts and a clean UI, it ensures that every product — from manufacturing to delivery — is verifiably authentic.

## 🌟 Key Features
- 🔄 Track product flow across **manufacturer → transporter → distributor → vendor**
- 🔐 Verify product authenticity using blockchain-backed smart contracts
- 👤 Secure user/admin registration and login via PostgreSQL
- ⛓️ Immutable product lifecycle logging with **Solidity smart contracts**
- 💻 Intuitive React frontend with a RESTful Node.js backend

## 🛠️ Tech Stack
- **Frontend:** React, Axios, Web3.js, React Router
- **Backend:** Node.js, Express, PostgreSQL
- **Blockchain:** Solidity, Hardhat, Ethereum (Sepolia testnet)

---

## 📁 Project Structure
```bash
trustdrive_mini_project/
├── contracts/           # Solidity smart contracts
│   └── smart_contract.sol
├── scripts/             # Deployment scripts using Hardhat
│   ├── deploy.js
│   └── final_deploy.js
├── trustdrive/          # Frontend (React)
│   ├── src/
│   └── ...
├── trustdrive_server/   # Backend (Node.js + PostgreSQL)
│   ├── server.js
│   ├── database.js
│   └── ...
├── hardhat.config.js    # Blockchain configuration
└── README.md            # Project documentation (this file)
```

---

## ⚙️ Prerequisites
- Node.js (v16+ recommended)
- npm
- PostgreSQL (for user data)
- [MetaMask](https://metamask.io/) (for blockchain wallet access)

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone <repo-url>
cd trustdrive_mini_project
```

### 2️⃣ Install Dependencies
```bash
cd trustdrive
npm install
cd ../trustdrive_server
npm install
cd ..
npm install  # For Hardhat dependencies
```

### 3️⃣ Configure Environment Variables
Create a `.env` file in the root with:
```
SEPOLIA_URL=<your_sepolia_rpc_url>
PRIVATE_KEY=<your_private_key>
```
Make sure to update DB credentials in `trustdrive_server/database.js`.

### 4️⃣ Deploy Smart Contract
```bash
npx hardhat run scripts/deploy.js --network sepolia
```
Save the deployed contract address for integration.

### 5️⃣ Start Backend Server
```bash
cd trustdrive_server
npm run dev
```

### 6️⃣ Start Frontend
```bash
cd trustdrive
npm start
```
Navigate to [http://localhost:3000](http://localhost:3000)

---

## 🧪 How to Use
- Register/login as **admin** or **user**
- Admin can add and update product details as they pass through the supply chain
- Users can view and verify a product’s lifecycle via blockchain verification

---

## 📜 Smart Contract Highlights
- Tracks a product's complete journey through the supply chain
- Functions include: addProduct, updateStage, verifyAuthenticity
- Immutable logs ensure no tampering or data loss

---

## 📂 Scripts
- `scripts/deploy.js`: Compiles and deploys contracts to Sepolia testnet
- `scripts/final_deploy.js`: Extended script with usage examples



---

> 💡 *TrustDrive brings truth to logistics. Because trust should be built-in — not assumed.*
