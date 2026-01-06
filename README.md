# AetherVault — NFT Auction & Marketplace DApp

## Overview
AetherVault is a decentralized NFT auction and marketplace built on Ethereum.
It allows users to mint NFTs, buy and sell at fixed prices, and participate in live timed auctions with real-time bidding and secure ownership transfers.

## Snapshot
Interactive NFT marketplace, live auction bidding, NFT minting flow, analytics dashboard, and account management views.
<img width="1705" height="859" alt="Screenshot 2026-01-05 at 9 13 20 PM" src="https://github.com/user-attachments/assets/109286f8-babb-407f-b19e-afd3e7d5e435" />


## Features

### NFT Management
- Mint ERC-721 NFTs with metadata stored on IPFS
- View and manage owned NFTs
- Transfer NFT ownership
- Real-time transaction updates via MetaMask

### Marketplace
- Browse NFTs listed for sale
- Buy NFTs instantly at fixed prices
- View detailed NFT metadata, ownership history, and pricing

### Auction System
- Create timed auctions for NFTs
- Participate in real-time bidding
- Automatic highest-bidder selection
- Claim NFTs after winning auctions
- Reclaim NFTs from unsold auctions

### Batch Minting
- Upload multiple NFT images in a single selection
- Auto-generate metadata for each NFT
- Mint multiple NFTs in one blockchain transaction
- Reduced gas cost per NFT

### IPFS Storage
- Decentralized storage using Pinata and IPFS
- Permanent, censorship-resistant NFT metadata
- No centralized server dependency

### Live Bidding
- Real-time bid placement using MetaMask
- Immediate blockchain updates for every bid
- On-chain bid validation and outbid detection

### Timed Auctions
- Custom auction starting prices
- Configurable auction durations
- Automated auction start and end handling
- Secure NFT escrow during active auctions

### Analytics Dashboard
- Total auctions, active auctions, and completed auctions
- Total trading volume and average sale price
- Price history and live auction charts

### User Experience
- MetaMask wallet integration
- Smooth blockchain interaction via ethers.js
- Responsive UI built with Tailwind CSS
- Clean navigation across marketplace, auctions, minting, analytics, and account

## Tech Stack

### Blockchain
- Solidity
- OpenZeppelin ERC-721
- Truffle
- Ganache
- Sepolia Testnet
- IPFS and Pinata

### Frontend
- React and Vite
- ethers.js
- Tailwind CSS
- Material UI
- Web3.js utilities

## Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/dgkans/AetherVaultBlockchain
cd AetherVault

# 2. Install root dependencies
npm install

# 3. Configure local blockchain (Ganache)
# - Start Ganache
# - Copy RPC URL and Network ID
# - Update truffle-config.js

# 4. Compile and deploy smart contracts
truffle compile
truffle migrate

# 5. Copy contract ABIs to frontend
cp build/contracts/Auction.json auction-frontend/src/abis/
cp build/contracts/NFTAuction.json auction-frontend/src/abis/

# 6. Configure Pinata credentials
# Edit: auction-frontend/src/pinata.js
# Add your Pinata API Key and Secret Key

# 7. Install frontend dependencies and run the app
cd auction-frontend
npm install
npm run dev
