# 🏥 Medical Record Storage DApp

A decentralized application (DApp) built on the Ethereum blockchain that gives patients complete control over their medical records with secure global access anytime, anywhere.

## 🌟 Features

- **🔒 Secure Storage**: Medical records stored immutably on the Ethereum blockchain
- **👤 Patient-Centric**: Patients have complete control over their data
- **🌍 Global Access**: Access medical records from anywhere in the world
- **📝 Easy Data Entry**: User-friendly interface for adding medical records
- **🔐 Authorized Access**: Controlled access system for healthcare providers
- **⛓️ Blockchain Security**: Leveraging Solidity smart contracts for data integrity
- **🎨 Modern UI**: Built with React for a seamless user experience

## 🛠️ Technology Stack

- **Smart Contracts**: Solidity ^0.8.18
- **Frontend**: React 18.2.0, Redux, React Router
- **Blockchain Development**: Hardhat
- **Wallet Integration**: MetaMask
- **Styling**: CSS3, Modern UI components
- **Testing**: Hardhat Test Suite

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v16-18 recommended)
- [Git](https://git-scm.com/)
- [MetaMask](https://metamask.io/) browser extension

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/sushantonwork/MedChain-Dapp.git
cd MedChain-Dapp
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```bash
# For Windows
New-Item .env -ItemType File

# For Linux/Mac
touch .env
```

Add the following content to your `.env` file:

```env
PRIVATE_KEYS=" "
GOERLI_API_KEY=" "
MUMBAI_API_KEY=" "
```

### 4. Compile Smart Contracts

```bash
npx hardhat compile
```

### 5. Run Tests

```bash
npx hardhat test
```

### 6. Start Local Blockchain

Open a new terminal window and run:

```bash
npx hardhat node
```

Keep this terminal running throughout development.

### 7. Deploy Smart Contracts

In your original terminal:

```bash
npx hardhat run scripts/00-deploy.js --network localhost
```

### 8. Launch the Application

```bash
npm start
```

The application will open at `http://localhost:3000`

## 🔧 MetaMask Configuration

### Add Local Network to MetaMask

1. Open MetaMask extension
2. Click network dropdown → "Add Network" → "Add a network manually"
3. Fill in the details:
   - **Network Name**: Localhost 8545
   - **New RPC URL**: http://127.0.0.1:8545
   - **Chain ID**: 31337
   - **Currency Symbol**: ETH
   - **Block Explorer URL**: (leave blank)

### Import Test Account

1. Copy a private key from your `npx hardhat node` terminal output
2. In MetaMask: Account icon → "Import Account"
3. Paste the private key and import

## 📁 Project Structure

```
medical-record-storage/
├── contracts/              # Solidity smart contracts
│   └── MedicalRecords.sol  # Main medical records contract
├── scripts/                # Deployment scripts
│   ├── 00-deploy.js        # Contract deployment script
│   └── 01-seeding.js       # Data seeding script
├── src/                    # React frontend application
│   ├── components/         # React components
│   ├── store/              # Redux store configuration
│   ├── abis/               # Contract ABIs
│   ├── assets/             # Static assets
│   └── config.json         # Contract addresses
├── test/                   # Smart contract tests
├── public/                 # Public static files
├── .env                    # Environment variables
├── hardhat.config.js       # Hardhat configuration
└── package.json            # Project dependencies
```

## 🎯 Smart Contract Functions

### Medical Records Contract

- `addRecord()` - Add a new medical record
- `getRecord(uint recordId)` - Retrieve a specific record
- `getAllRecords()` - Get all records for the connected account
- `updateRecord()` - Update existing record
- `deleteRecord()` - Mark record as deleted

## 🔥 Available Scripts

### Blockchain Commands
```bash
npx hardhat compile          # Compile smart contracts
npx hardhat test            # Run contract tests
npx hardhat node            # Start local blockchain
npx hardhat run scripts/00-deploy.js --network localhost  # Deploy contracts
```

### Frontend Commands
```bash
npm start                   # Start development server
npm build                   # Build for production
npm test                    # Run React tests
npm run eject               # Eject from Create React App
```

## 🌐 Deployment

### Local Development
Follow the Quick Start guide above for local development.

### Testnet Deployment

1. **Get testnet ETH** from faucets:
   - [Goerli Faucet](https://goerlifaucet.com/)
   - [Mumbai Faucet](https://faucet.polygon.technology/)

2. **Update your `.env`** with real API keys:
   ```env
   PRIVATE_KEYS=your_real_private_key_here
   GOERLI_API_KEY=https://goerli.infura.io/v3/your_infura_project_id
   MUMBAI_API_KEY=https://polygon-mumbai.g.alchemy.com/v2/your_alchemy_key
   ```

3. **Deploy to testnet**:
   ```bash
   # Deploy to Goerli
   npx hardhat run scripts/00-deploy.js --network goerli
   
   # Deploy to Mumbai
   npx hardhat run scripts/00-deploy.js --network mumbai
   ```

## 🧪 Testing

Run the comprehensive test suite:

```bash
# Run all tests
npx hardhat test

# Run tests with gas reporting
REPORT_GAS=true npx hardhat test

# Run specific test file
npx hardhat test test/MedicalRecords.test.js
```

## 🛡️ Security Features

- **Immutable Records**: Once stored, medical records cannot be altered
- **Access Control**: Only authorized users can access specific records
- **Decentralized Storage**: No single point of failure
- **Privacy Protection**: Patient data is encrypted and secured
- **Audit Trail**: All transactions are recorded on the blockchain

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: (https://github.com/sushantonwork)
- LinkedIn: https://www.linkedin.com/in/sushant-kachhap-4153b1266/
- Email: sushantkachhap68@gmail.com

## 🙏 Acknowledgments

- Hardhat development framework
- OpenZeppelin for smart contract libraries
- React community for excellent documentation
- Ethereum community for blockchain innovation
