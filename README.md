# Transparent Donation System

## Team Information
- **Team ID**: T103  
- **Team Name**: Cursor  

### Members
- Bakshish – Backend Developer  
- Pianshu – Frontend Developer  
- Nidhi – UI Designing 
- Komal – Feature Enhancement  
- Aishwarya – Blockchain Engineer

---

## Problem Statement
Current charity platforms in India lack transparency and verifiable proof of impact. Donors often cannot see exactly how their contributions are used, while NGOs struggle to build trust.  

**Our solution:**  
A **blockchain-powered Transparent Donation System** that ensures every step of the donation process is visible, verifiable, and tamper-proof.  

- NGOs can create campaigns with milestones.  
- Donors can contribute using **simulated UPI payments**.  
- Proofs (media, geo-tags) are stored on **IPFS** and anchored to **Polygon Amoy testnet**.  
- Donors are rewarded with **NFT badges (Impact Tokens)**.  
- A public **Transparency Dashboard** shows live progress, proofs, and impact maps.  

---

## Tech Stack
- **Frontend**: React + TailwindCSS + Chart.js + Leaflet.js  
- **Backend**: Node.js + Express.js  
- **Database**: MongoDB Atlas (Free Tier)  
- **Blockchain**: Hardhat + Ethers.js + Polygon Amoy Testnet  
- **Storage**: IPFS (via Web3.Storage / NFT.Storage)  
- **Authentication**: JWT  
- **Payments**: Simulated UPI QR flow  

---

## How to Run the Project

### 1. Clone Repository
```bash
git clone <your-forked-repo-url>
cd submissions/T103_Cursor/code
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment
Create a `.env` file in the root with:
```env
PORT=5000
MONGODB_URI=<your_mongodb_uri>
JWT_SECRET=<your_jwt_secret>
POLYGON_RPC_URL=https://polygon-amoy.g.alchemy.com/v2/<your_alchemy_api_key>
PRIVATE_KEY=<your_wallet_private_key>
NFT_STORAGE_API_KEY=<your_nft_storage_api_key>
NODE_ENV=development
```

### 4. Compile & Deploy Contracts
```bash
npx hardhat compile
npx hardhat run scripts/deploy.js --network amoy
```

This will generate deployed contract addresses in `/config/contracts.json`.

### 5. Run Backend Server
```bash
npm start
```
Server runs on: [http://localhost:5000](http://localhost:5000)

### 6. Run Frontend
```bash
cd frontend
npm install
npm start
```
Frontend runs on: [http://localhost:3000](http://localhost:3000)

---

## Special Notes
- Uses **Polygon Amoy Testnet** for blockchain integration (free test MATIC required via faucet).  
- Donations are simulated with UPI QR (no real money).  
- Proofs stored on **IPFS** via free Web3.Storage/NFT.Storage APIs.  
- NFT rewards minted on Polygon (ERC-721 standard).  
- Presentation file included as: `T103_Cursor_Presentation.pdf`.  

---

## Credits
- **OpenZeppelin Contracts** (ERC-721 NFT standard)  
- **Polygon Amoy Testnet** (for blockchain deployment)  
- **IPFS / NFT.Storage** (for decentralized file storage)  
- **Chart.js / Leaflet.js** (for dashboard visualization)  
- **Alchemy** (RPC provider)  
