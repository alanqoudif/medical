# Medical System (النظام الطبي)

## Description (الوصف)
A comprehensive medical system built with modern web technologies to manage patient records, appointments, and medical transactions with secure encryption.

## Features (المميزات)
- Patient management (إدارة المرضى)
- Appointment scheduling (جدولة المواعيد)
- Secure data encryption (تشفير البيانات بشكل آمن)
- Medical records management (إدارة السجلات الطبية)
- Prescription management (إدارة الوصفات الطبية)

## Technologies Used (التقنيات المستخدمة)
- Next.js
- TypeScript
- Supabase
- Tailwind CSS
- Prisma
- NextAuth.js

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
Create a `.env` file in the root directory and add the following:
```env
DATABASE_URL="your-database-url"
NEXTAUTH_SECRET="your-nextauth-secret"
NEXTAUTH_URL="http://localhost:3000"
SUPABASE_URL="your-supabase-url"
SUPABASE_ANON_KEY="your-supabase-anon-key"
```

4. Run database migrations (تشغيل ترحيل قاعدة البيانات):
```bash
npx prisma migrate dev
```

5. Start the development server (تشغيل خادم التطوير):
```bash
npm run dev
```

## Data Security (أمن البيانات)

### Encryption Implementation (تنفيذ التشفير)
- All sensitive data is encrypted using AES-256-GCM encryption
- Patient data is encrypted at rest and in transit
- Unique encryption keys for each patient record
- Secure key management using AWS KMS

### Security Measures (إجراءات الأمان)
1. End-to-end encryption for all sensitive data
2. Role-based access control (RBAC)
3. Audit logging for all data access
4. Regular security updates and patches
5. Compliance with healthcare data protection standards

## Usage (الاستخدام)

1. Login with your credentials (تسجيل الدخول):
   - Access the system at `http://localhost:3000`
   - Enter your username and password

2. Navigate the dashboard (استخدام لوحة التحكم):
   - View patient records
   - Schedule appointments
   - Manage prescriptions
   - Generate reports

## API Documentation (توثيق واجهة البرمجة)

### Authentication (المصادقة)
```typescript
POST /api/auth/login
POST /api/auth/logout
POST /api/auth/refresh
```

### Patient Management (إدارة المرضى)
```typescript
GET /api/patients
POST /api/patients
PUT /api/patients/:id
DELETE /api/patients/:id
```

### Appointments (المواعيد)
```typescript
GET /api/appointments
POST /api/appointments
PUT /api/appointments/:id
DELETE /api/appointments/:id
```

## Contributing (المساهمة)
Contributions are welcome! Please feel free to submit a Pull Request.

## License (الترخيص)
This project is licensed under the MIT License - see the LICENSE file for details.

## Support (الدعم)
For support, please email support@example.com or open an issue in the GitHub repository.
