# Medical System (النظام الطبي)

## Description (الوصف)
A comprehensive medical system built with blockchain technology to manage patient records, appointments, and medical transactions securely on the Ethereum network.

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
   - Connect to Holesky testnet
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
