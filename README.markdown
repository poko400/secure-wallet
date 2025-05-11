# Secure Web3 Wallet App

This project is a secure Web3 application that allows users to connect their MetaMask wallet, deposit Ether into a smart contract, withdraw Ether, and view balances. It includes a Solidity smart contract (`SecureWallet.sol`) and a front-end (`index.html`).

## Files
- **SecureWallet.sol**: The smart contract for depositing and withdrawing Ether.
- **index.html**: The front-end interface for interacting with the contract via MetaMask.
- **README.md**: This file with setup instructions.

## Prerequisites
- **MetaMask**: Install the MetaMask browser extension (https://-metamask.io).
- **Test ETH**: Get test Ether for the Sepolia testnet (e.g., from https://sepoliafaucet.com).
- **Node.js** (optional): For local hosting or Vercel deployment.
- **Text Editor**: To edit `index.html` (e.g., VS Code).

## Setup Instructions

### Step 1: Deploy the Smart Contract
1. **Open Remix**:
   - Go to https://remix.ethereum.org.
   - Create a new file named `SecureWallet.sol` and paste the contract code.
2. **Compile**:
   - In the “Solidity Compiler” tab, select version `0.8.20`.
   - Click “Compile SecureWallet.sol”.
3. **Deploy**:
   - Go to the “Deploy & Run Transactions” tab.
   - Set “Environment” to “Injected Provider - MetaMask”.
   - Connect MetaMask, ensuring you’re on the Sepolia testnet.
   - Select `SecureWallet` and click “Deploy”. Confirm the transaction in MetaMask.
4. **Get Contract Address**:
   - Copy the deployed contract address from Remix (under “Deployed Contracts”).
   - Open `index.html` in a text editor and replace `YOUR_CONTRACT_ADDRESS_HERE` with the contract address.

### Step 2: Host the Front-End
Choose one of the following hosting options.

#### Option 1: Vercel (Recommended)
1. **Sign Up**:
   - Create an account at https://vercel.com.
   - Install the Vercel CLI: `npm install -g vercel`.
2. **Deploy**:
   - Create a folder (e.g., `web3-wallet-app`) and place `index.html` in it.
   - In the terminal, navigate to the folder: `cd web3-wallet-app`.
   - Run `vercel` and follow the prompts to deploy.
   - Vercel will provide a URL (e.g., `https://your-app-name.vercel.app`).
3. **Access**:
   - Open the URL in a browser with MetaMask installed.

#### Option 2: Netlify
1. **Sign Up**:
   - Create an account at https://www.netlify.com.
2. **Deploy**:
   - Drag and drop `index.html` into Netlify’s “Sites” dashboard.
   - Netlify will provide a URL (e.g., `https://your-app-name.netlify.app`).
3. **Access**:
   - Open the URL in a browser with MetaMask.

#### Option 3: Local Server
1. **Run**:
   - Install Node.js (https://nodejs.org).
   - Navigate to the folder containing `index.html`.
   - Run `npx serve`.
2. **Access**:
   - Open the provided URL (e.g., `http://localhost:3000`) in a browser.

### Step 3: Test the App
1. **Connect Wallet**:
   - Open the hosted URL in a browser with MetaMask on the Sepolia testnet.
   - Click “Connect Wallet” and approve in MetaMask.
   - Verify your wallet address and balance display.
2. **Deposit**:
   - Enter a small amount (e.g., 0.01 ETH) and click “Deposit”.
   - Confirm the transaction in MetaMask.
   - Check that the contract balance updates.
3. **Withdraw**:
   - Enter an amount (e.g., 0.01 ETH) and click “Withdraw”.
   - Confirm in MetaMask.
   - Verify your wallet balance updates.
4. **View Balances**:
   - Ensure contract and user balances display correctly.

### Troubleshooting
- **“Invalid Contract Address”**: Verify the `contractAddress` in `index.html` matches the deployed contract.
- **“Insufficient Funds”**: Get more test ETH from a Sepolia faucet.
- **“MetaMask Not Detected”**: Install or unlock MetaMask.
- **“Transaction Failed”**: Check gas limits or ensure you’re on Sepolia.
- **UI Not Loading**: Confirm the file is hosted correctly.

### Security Notes
- **Testnet Only**: Use Sepolia to avoid risking real funds.
- **Audit Contract**: Verify the contract on Sepolia Etherscan.
- **No Hidden Scripts**: Inspect `index.html` for transparency.
- **User Confirmation**: All transactions require MetaMask approval.

## Next Steps
- Add transaction history using contract events.
- Support ERC-20 tokens (e.g., USDC).
- Optimize the UI for mobile devices.
- Deploy to a custom domain for a professional look.

For help, contact the developer or refer to:
- Remix: https://remix.ethereum.org
- Vercel: https://vercel.com
- Netlify: https://www.netlify.com
- MetaMask: https://metamask.io