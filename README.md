# TrustDrive: Blockchain-based Supply Chain Management

TrustDrive is a decentralized application (dApp) for tracking and verifying products across a supply chain using blockchain technology. It ensures transparency and authenticity from manufacturer to end vendor.

## Features
- Track products through manufacturer, transporter, distributor, and vendor stages
- Verify product genuineness using blockchain
- User and admin registration/login with PostgreSQL database
- Smart contract for immutable product tracking
- Modern React frontend and RESTful backend API

## Tech Stack
- **Frontend:** React, Axios, Web3.js, React Router
- **Backend:** Node.js, Express, PostgreSQL
- **Blockchain:** Solidity, Hardhat, Ethereum (Sepolia testnet)

## Directory Structure
```
trustdrive_mini_project/
├── contracts/           # Solidity smart contract(s)
│   └── smart_contract.sol
├── scripts/             # Hardhat deployment scripts
│   ├── deploy.js
│   └── final_deploy.js
├── trustdrive/          # React frontend
│   ├── src/
│   └── ...
├── trustdrive_server/   # Node.js backend
│   ├── server.js
│   ├── database.js
│   └── ...
├── hardhat.config.js    # Hardhat configuration
└── README.md            # Project documentation (this file)
```

## Prerequisites
- Node.js (v16+ recommended)
- npm
- PostgreSQL
- [Metamask](https://metamask.io/) (for interacting with the dApp)

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repo-url>
cd trustdrive_mini_project
```

### 2. Install Dependencies
Install for each subproject:
```bash
cd trustdrive
npm install
cd ../trustdrive_server
npm install
cd ..
npm install   # For Hardhat and scripts
```

### 3. Configure Environment
- **PostgreSQL:**
  - Create a database (default: `mini_project`)
  - Update credentials in `trustdrive_server/database.js` if needed
- **Hardhat:**
  - Create a `.env` file in the root with:
    ```
    SEPOLIA_URL=<your_sepolia_rpc_url>
    PRIVATE_KEY=<your_private_key>
    ```

### 4. Deploy the Smart Contract
```bash
npx hardhat run scripts/deploy.js --network sepolia
```
- Note the deployed contract address for frontend/backend integration.

### 5. Start the Backend Server
```bash
cd trustdrive_server
npm run dev
```

### 6. Start the Frontend
```bash
cd trustdrive
npm start
```
- The app will be available at [http://localhost:3000](http://localhost:3000)

## Usage
- Register and login as admin or user
- Add and track products through the supply chain
- Verify product authenticity using the blockchain

## Smart Contract Overview
- Written in Solidity (`contracts/smart_contract.sol`)
- Tracks product lifecycle: manufacturer → transporter → distributor → vendor
- Provides functions to add and retrieve product details, and check genuineness

## Scripts
- `scripts/deploy.js`: Deploys the smart contract and demonstrates usage

## License
This project is licensed under the MIT License.
