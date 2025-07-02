🛡️ Zama Developer Program – Level 2 Guide (100% Working on Codespace)
Complete Level 2 of the Zama Developer Program using GitHub Codespace — clean, fast, and tested ✅

✅ Level 2: “Write Your First Confidential Smart Contract”
🔹 STEP 1: Open Template in Codespace
Go to 👉 https://github.com/zama-ai/fhevm-hardhat-template
Click the green Code button
Select → Open with Codespaces → + New codespace
Wait for Codespace to fully load and initialize
🔹 Step 2: Clean and Recreate Contracts Folder
rm -rf contracts/*
mkdir contracts
touch contracts/Calculator.sol
🔹 Step 3: Add Calculator Contract
Open contracts
Right Click
Add file
Create /Calculator.sol and paste this code:
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Calculator {
    function encryptedAdd(uint32 a, uint32 b) public pure returns (uint32) {
        return a + b;
    }
}
🔹 Step 4: Install Required Packages
npm install
npm install @fhenixprotocol/contracts --save
🔹 Step 5: Compile the Contract
npx hardhat compile
Output should show: Compiled 1 Solidity file successfully

🔹 Step 6: Claim Level 2 on Guild - https://guild.xyz/zama/developer-program
✅ Level 3: “Submit Contract Address”
🔹 Step 1: Create scripts Folder
mkdir scripts
🔹 Step 2: Create Deploy Script File
touch scripts/deploy.js
• Then in Codespace (left sidebar):

→ Open scripts/deploy.js → Paste the following code:

const hre = require("hardhat");

async function main() {
  const Calculator = await hre.ethers.getContractFactory("Calculator");
  const calculator = await Calculator.deploy();
  await calculator.waitForDeployment();

  console.log("Calculator deployed to:", await calculator.getAddress());
}

main().catch((error) => {
  console.error(error);
  process.exitCode = 1;
});
🔹 Step 3: Deploy the Contract
Run this in terminal:

npx hardhat run scripts/deploy.js
Expected output:

Calculator deployed to: 0xAbC...123
That address is your deployed smart contract address.

🔹 Step 4: Claim Level 3
Visit: https://guild.xyz/zama/developer-program

→ Find Level 3: Deploy your confidential contract → Paste your deployed contract address

🎉 You’ve completed Level 3!

🙌 Guide Created by: @EarnByAbhi
Follow & Stay Connected for More Zama Alpha, Airdrops & Dev Tutorials

📍 X (Twitter): @EarnByAbhi
💬 Telegram: @EarnByAbhi23
▶️ YouTube: EarnByAbhi
🧠 Join our Telegram Community
For live help, updates, & early alpha drops
👉 https://t.me/earnbyabhi23

About
No description, website, or topics provided.
Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 0 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Footer
© 2025 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact
Manage cookies# Zama-Dev
