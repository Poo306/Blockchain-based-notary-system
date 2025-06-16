Blockchain Notary

**Blockchain Notary** is a minimal, logical, and practical decentralized application (DApp) that uses smart contracts on Ethereum to **notarize any digital document hash securely and immutably**.

---

Demo

🔗 Live Demo: [http://18.157.182.120:8000/](http://18.157.182.120:8000/)

---

Concept

Traditionally, to prove ownership of a document at a specific point in time, you’d visit a **notary public**. But now, you can do the same using **blockchain technology** — cheaper, faster, and globally verifiable.

This DApp **registers a unique cryptographic hash** of your document onto the blockchain — meaning:

- No document is ever uploaded or shared
- Only a **SHA-256 hash** of the file is stored
- Anyone can later verify the document’s authenticity
- The data is immutable and permanent

---

How It Works

1. A user selects a document (e.g., PDF, image).
2. The app computes its **SHA-256 hash**.
3. That hash is submitted to the **Notarise smart contract**.
4. The contract logs the `msg.sender` and `timestamp`.
5. The file hash can be queried anytime to verify ownership and time.

---

Technologies Used

- **Solidity** — for the Notarise smart contract  
- **Hardhat** — development and testing framework  
- **Ganache** or **Hardhat Network** — local blockchain simulation  
- **Node.js & Ethers.js** — for backend scripting  
- (Optional) HTML/JS frontend  

---

Project Structure

blockchain-notary/
├── contracts/
│ └── Notarise.sol # Smart contract
├── scripts/
│ ├── deploy.cjs # Deployment script
│ └── interact.cjs # Interaction script
├── hardhat.config.js # Hardhat configuration
├── package.json
├── .gitignore
└── README.md

---

Setup Instructions

1. **Clone this repo**
   ```bash
   git clone https://github.com/Poo306/blockchain-notary.git
   cd blockchain-notary
Install dependencies
   npm install

Run Ganache or Hardhat local node
   npx hardhat node

Deploy the contract
   npx hardhat run scripts/deploy.cjs --network localhost

Run the interaction script
   npx hardhat run scripts/interact.cjs --network localhost

Privacy Notice
We never upload your actual file. Only the hash is registered.
Your document remains 100% private and secure.

License
This project is licensed under the BSD-2-Clause License.

Acknowledgments
This project is originally based on the open-source Blockchain Notary DApp by Jan Paricka, licensed under the BSD 2-Clause License.

Modifications in this fork include:

Improved deployment and interaction scripts

Updated error handling and console output

Clarified usage and setup steps

Integration testing with Ganache and Hardhat

All original license terms are respected and retained.

Notice
This repository contains modifications of the original "Blockchain Notary" by Jan Paricka (2018),
licensed under the BSD-2-Clause License. The modifications were made by Pooja R in 2025 for academic purposes.

Donation
If you liked this project, consider donating:

ETH: 0xbcFAB06E0cc4Fe694Bdf780F1FcB1bB143bD93Ad
