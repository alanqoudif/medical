# Medical System (النظام الطبي)

## Description (الوصف)
A comprehensive medical system built with blockchain technology to manage patient records, appointments, and medical transactions securely on the Ethereum network.

## Prerequisites (المتطلبات الأساسية)

### MetaMask Wallet Setup (إعداد محفظة MetaMask)

1. Install MetaMask (تثبيت المحفظة):
   - [Watch Tutorial: How to Create Free MetaMask Wallet](https://www.youtube.com/watch?v=MlmAeyhGMbU)
   - Install from [MetaMask Official Website](https://metamask.io/)
   - Available for Chrome, Firefox, Brave, and Edge

2. Configure Holesky Network (إعداد شبكة Holesky):
   - Network Name: Holesky Test Network
   - New RPC URL: https://ethereum-holesky.publicnode.com
   - Chain ID: 17000
   - Currency Symbol: ETH
   - Block Explorer URL: https://holesky.etherscan.io

3. Get Test ETH (الحصول على ETH تجريبي):
   - Visit [Holesky Faucet](https://holesky-faucet.pk910.de/)
   - Enter your wallet address
   - Receive free test ETH

### Node.js Setup (إعداد Node.js)

1. Install NVM (Node Version Manager):
```bash
# For macOS/Linux
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# For Windows - using PowerShell (Run as Administrator)
winget install CoreyButler.NVMforWindows
```

2. Install and use Node.js v18.17.1:
```bash
# Install specific version
nvm install 18.17.1

# Use the installed version
nvm use 18.17.1
```

3. Verify installation:
```bash
node --version
# Should output: v18.17.1
```

### Local Development Network (شبكة التطوير المحلية)

You can use either:

1. Holesky Testnet (الشبكة التجريبية):
   - Production-like environment
   - Requires test ETH
   - Real blockchain interactions

2. Local Hardhat Network (الشبكة المحلية):
   - For development and testing
   - Instant transactions
   - Free test ETH
   - No real blockchain costs

#### MetaMask Configuration for Local Network (إعداد MetaMask للشبكة المحلية)
1. Network Name: localhost
2. RPC URL: http://127.0.0.1:8545
3. Chain ID: 1337
4. Currency Symbol: ETH

#### Hardhat Local Network (شبكة Hardhat المحلية)
```bash
# Start local blockchain
npm run node
```

Default Admin Account:
- Address: 0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266
- Balance: 10000 ETH

**Note**: When switching accounts in MetaMask, clear your transaction history to avoid conflicts.

## Features (المميزات)
- Patient management (إدارة المرضى)
- Appointment scheduling (جدولة المواعيد)
- Secure blockchain-based data storage (تخزين البيانات على البلوكتشين)
- Medical records management (إدارة السجلات الطبية)
- Prescription management (إدارة الوصفات الطبية)
- Smart contract integration (تكامل العقود الذكية)

## Technologies Used (التقنيات المستخدمة)
- Next.js
- Ethereum Blockchain
- Web3.js
- IPFS/Pinata
- Smart Contracts (Solidity)
- OpenAI Integration
- Hardhat (Development Environment)

## Installation (التثبيت)

1. Clone the repository (نسخ المشروع):
```bash
git clone https://github.com/alanqoudif/medical.git
cd medical
```

2. Install dependencies (تثبيت المتطلبات):
```bash
npm install
```

3. Set up environment variables (إعداد متغيرات البيئة):
Create a `.env.local` file in the root directory and add the following:
```env
# Contract Address
NEXT_PUBLIC_HEALTH_CARE=your_contract_address

# OpenAI API Key
NEXT_PUBLIC_OPEN_AI_KEY=your_openai_api_key

# Transaction Fees (in ETH)
NEXT_PUBLIC_DOCTOR_REGISTER_FEE=0.0025
NEXT_PUBLIC_PATIENT_APPOINMENT_FEE=0.0025
NEXT_PUBLIC_PATIENT_REGISTER_FEE=0.00025

# Network Configuration
NEXT_PUBLIC_NETWORK=holesky
NEXT_PUBLIC_CURRENCY=ETH

# Admin Address
NEXT_PUBLIC_ADMIN_ADDRESS=your_admin_wallet_address

# Pinata (IPFS) Configuration
NEXT_PUBLIC_PINATA_API_KEY=your_pinata_api_key
NEXT_PUBLIC_PINATA_SECRET_KEY=your_pinata_secret_key
NEXT_PUBLIC_RPC_URL=your_ethereum_rpc_url
```

4. Start the development server (تشغيل خادم التطوير):
```bash
npm run dev
```

## Blockchain Integration (تكامل البلوكتشين)

### Smart Contract Details (تفاصيل العقد الذكي)
- Network: Holesky (Ethereum Testnet)
- Currency: ETH
- Contract Address: Check `.env.local` file

### Transaction Fees (رسوم المعاملات)
- Doctor Registration: 0.0025 ETH
- Patient Registration: 0.00025 ETH
- Appointment Booking: 0.0025 ETH

## Data Security (أمن البيانات)

### Security Implementation (تنفيذ الأمان)
- Decentralized data storage using IPFS
- Smart contract-based access control
- Encrypted medical records on IPFS
- Blockchain-based audit trail
- Secure key management

## Usage (الاستخدام)

1. Connect Wallet (ربط المحفظة):
   - Install MetaMask or compatible Web3 wallet
   - Connect to Holesky testnet or local network
   - Ensure you have sufficient ETH for transactions

2. Navigate the dashboard (استخدام لوحة التحكم):
   - Register as doctor/patient
   - Manage appointments
   - Access medical records
   - Process prescriptions

## Smart Contract Functions (وظائف العقد الذكي)

### Patient Management (إدارة المرضى)
```solidity
registerPatient()
updatePatientDetails()
getPatientRecords()
```

### Doctor Management (إدارة الأطباء)
```solidity
registerDoctor()
updateDoctorDetails()
getDoctorAvailability()
```

### Appointments (المواعيد)
```solidity
bookAppointment()
cancelAppointment()
updateAppointmentStatus()
```

## Contributing (المساهمة)
Contributions are welcome! Please feel free to submit a Pull Request.

## License (الترخيص)
This project is licensed under the MIT License - see the LICENSE file for details.

## Support (الدعم)
For support, please email info@nuqtai.com or open an issue in the GitHub repository.

## Deployment on Netlify (النشر على Netlify)

1. Create a Netlify Account (إنشاء حساب على Netlify):
   - Visit [Netlify](https://www.netlify.com/)
   - Sign up for a free account

2. Prepare Your Project (تجهيز المشروع):
   ```bash
   # Build your project
   npm run build
   ```

3. Deploy via Netlify UI (النشر عبر واجهة Netlify):
   - Log in to Netlify
   - Drag and drop your `out` or `build` folder to Netlify
   - Wait for deployment to complete

4. Deploy via Netlify CLI (النشر عبر واجهة سطر الأوامر):
   ```bash
   # Install Netlify CLI
   npm install netlify-cli -g

   # Login to Netlify
   netlify login

   # Initialize your site
   netlify init

   # Deploy your site
   netlify deploy --prod
   ```

5. Configure Environment Variables (إعداد متغيرات البيئة):
   - Go to Site settings > Build & deploy > Environment
   - Add all variables from your `.env.local` file
   - Redeploy your site

6. Setup Custom Domain (إعداد نطاق مخصص) - Optional:
   - Go to Domain settings
   - Add your custom domain
   - Configure DNS settings

## Graduation Project Defense FAQ (أسئلة متوقعة في مناقشة مشروع التخرج)

### Project Overview (نظرة عامة على المشروع)

1. **What problem does your project solve? (ما هي المشكلة التي يحلها مشروعك؟)**
   - The project addresses the need for secure, transparent medical record management
   - Solves issues of data privacy and accessibility in healthcare
   - Reduces paperwork and administrative overhead
   - Enables secure sharing of medical records between healthcare providers

2. **Why did you choose blockchain technology? (لماذا اخترت تقنية البلوكتشين؟)**
   - Immutable record-keeping
   - Decentralized data storage
   - Enhanced security and transparency
   - Smart contract automation
   - Patient data ownership and control

### Technical Implementation (التنفيذ التقني)

3. **How does the encryption system work? (كيف يعمل نظام التشفير؟)**
   - Patient data is encrypted before being stored on IPFS
   - Each record has a unique encryption key
   - Smart contracts manage access control
   - Only authorized parties can decrypt and access records
   - Implementation uses industry-standard encryption algorithms

4. **Explain the smart contract architecture (اشرح هيكلية العقود الذكية)**
   - Main Healthcare contract manages core functionality
   - Separate structs for Patients, Doctors, and Medical Records
   - Access control modifiers ensure security
   - Event system for tracking changes
   - Gas-optimized operations

5. **How do you ensure data privacy? (كيف تضمن خصوصية البيانات؟)**
   - Off-chain storage of sensitive data using IPFS
   - On-chain storage of access controls and metadata
   - Role-based access control
   - Encrypted data transmission
   - Audit trail of all access attempts

### Security Measures (إجراءات الأمان)

6. **What security measures are implemented? (ما هي إجراءات الأمان المطبقة؟)**
   - Smart contract access controls
   - Data encryption at rest and in transit
   - Secure key management
   - Regular security audits
   - Compliance with healthcare data regulations

7. **How do you handle potential attacks? (كيف تتعامل مع الهجمات المحتملة؟)**
   - Input validation in smart contracts
   - Rate limiting for API calls
   - Protection against reentrancy attacks
   - Secure random number generation
   - Emergency stop functionality

### Scalability and Performance (قابلية التوسع والأداء)

8. **How scalable is the system? (ما مدى قابلية النظام للتوسع؟)**
   - Uses IPFS for distributed storage
   - Optimized smart contract operations
   - Batch processing capabilities
   - Efficient data indexing
   - Load balancing implementation

9. **What are the performance considerations? (ما هي اعتبارات الأداء؟)**
   - Transaction confirmation times
   - Gas optimization techniques
   - IPFS content addressing
   - Caching strategies
   - Network latency handling

### Future Improvements (التحسينات المستقبلية)

10. **What future improvements could be made? (ما هي التحسينات المستقبلية الممكنة؟)**
    - Integration with more healthcare providers
    - Enhanced AI-powered diagnostics
    - Mobile application development
    - Additional blockchain network support
    - Advanced analytics capabilities

### Project Impact (تأثير المشروع)

11. **What is the potential impact of your project? (ما هو التأثير المحتمل لمشروعك؟)**
    - Improved patient care through better record access
    - Reduced healthcare costs
    - Enhanced data security and privacy
    - Streamlined healthcare operations
    - Better collaboration between healthcare providers

### Technical Challenges (التحديات التقنية)

12. **What were the main technical challenges? (ما هي التحديات التقنية الرئيسية؟)**
    - Implementing secure encryption
    - Gas optimization for smart contracts
    - IPFS integration and management
    - User interface design for Web3
    - Cross-platform compatibility
