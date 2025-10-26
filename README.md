# GoldenBlood 🩸

## 1. Overview

GoldenBlood is a comprehensive web-based blood donation and sales management system designed to streamline the entire blood transfusion ecosystem. The platform serves as a bridge between blood donors, recipients, and blood banks, facilitating secure blood transactions while maintaining an efficient inventory management system.

## 2. Motivation & Impact

The healthcare industry faces critical challenges in blood supply management, including:
- Inefficient tracking of blood donations and inventory
- Lack of transparency in the blood supply chain
- Time-consuming manual processes for donor-recipient matching
- Limited accessibility to real-time blood availability information

GoldenBlood addresses these challenges by providing a digital solution that:
- **Saves Lives**: Connects donors with recipients faster, reducing response time in emergencies
- **Enhances Transparency**: Provides real-time visibility into blood stock levels and donation history
- **Improves Efficiency**: Automates donor registration, blood typing, and inventory management
- **Ensures Safety**: Implements rigorous data validation and secure transaction protocols

## 3. How It Works

### Process Flow

**For Donors:**
1. Register and create a donor profile with blood type information
2. Schedule donation appointments through the platform
3. Receive notifications about donation opportunities and urgent needs
4. Track donation history and contribution impact

**For Recipients:**
1. Submit blood requests with specific requirements (blood type, quantity)
2. Search available blood inventory in real-time
3. Process secure transactions for blood procurement
4. Receive status updates on request fulfillment

**For Administrators:**
1. Manage donor and recipient databases
2. Monitor and update blood stock levels
3. Process and approve blood transactions
4. Generate reports on donation trends and inventory analytics

### Data Management

- **Donor Management**: Comprehensive profiles including blood type, contact information, donation history, and eligibility status
- **Recipient Management**: Request tracking, blood type matching, and transaction history
- **Stock Management**: Real-time inventory tracking with automated alerts for low stock levels, expiration date monitoring, and blood type distribution
- **Transaction Records**: Complete audit trail of all blood donations, sales, and transfers with timestamps and user accountability

## 4. Tech Stack

### Frontend
- **Next.js** - React framework for server-side rendering and optimal performance
- **Tailwind CSS** - Utility-first CSS framework for responsive design
- **TypeScript** - Type-safe development for enhanced code quality

### Backend
- **Next.js API Routes** - Serverless API endpoints
- **Prisma ORM** - Type-safe database access and migrations
- **PostgreSQL/MySQL** - Relational database for structured data storage

### Authentication & Security
- **NextAuth.js** - Secure authentication with multiple provider support
- **bcrypt** - Password hashing and encryption

### Development Tools
- **ESLint** - Code linting and quality enforcement
- **Prettier** - Code formatting
- **PostCSS** - CSS processing and optimization

## 5. Key Features

### 🔒 Secure Transactions
- End-to-end encryption for sensitive donor/recipient data
- Role-based access control (Admin, Donor, Recipient)
- Secure payment processing for blood sales
- HIPAA-compliant data handling practices

### 🛡️ Reliability
- Robust error handling and validation
- Database transaction consistency
- Automated backup systems
- 99.9% uptime SLA

### ⚡ Efficiency
- Real-time blood inventory updates
- Automated donor-recipient matching algorithms
- Quick search and filter capabilities
- Mobile-responsive design for on-the-go access
- Automated email notifications for critical events

### 📊 Additional Features
- Blood donation analytics dashboard
- Expiration date tracking and alerts
- Multi-language support
- Export functionality for reports (PDF, CSV)
- Emergency blood request prioritization

## 6. Setup & Installation Walkthrough

### Prerequisites

```bash
Node.js >= 18.0.0
npm or yarn
PostgreSQL or MySQL database
Git
```

### Step-by-Step Installation

**1. Clone the Repository**

```bash
git clone https://github.com/Adnane-Ahroum/GoldenBlood.git
cd GoldenBlood
```

**2. Install Dependencies**

```bash
npm install
# or
yarn install
```

**3. Environment Configuration**

Copy the example environment file and configure your variables:

```bash
cp .env.example .env
```

Edit `.env` with your configuration:

```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/goldenblood"

# NextAuth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key-here"

# Email Configuration (optional)
EMAIL_SERVER="smtp://username:password@smtp.example.com:587"
EMAIL_FROM="noreply@goldenblood.com"
```

**4. Database Setup**

Generate Prisma client and run migrations:

```bash
npx prisma generate
npx prisma migrate dev --name init
```

Seed the database (optional):

```bash
npx prisma db seed
```

**5. Run Development Server**

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

**6. Build for Production**

```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Troubleshooting

- **Database Connection Issues**: Verify your `DATABASE_URL` in `.env` is correct
- **Port Already in Use**: Change the port using `PORT=3001 npm run dev`
- **Prisma Errors**: Try `npx prisma generate` and restart the dev server

## 7. ER Diagram & Documentation

### Entity Relationship Diagram

The complete database schema and relationships are documented in:
- 📄 [Database ER Diagram (PDF)](./Database%20ER%20diagram.pdf)
- 📄 [Database Systems Proposal (PDF)](./Database%20systems%20proposal.pdf)
- 📄 [Final Report (PDF)](./Final%20Report.pdf)

### Key Entities

- **Users**: Stores user credentials and roles
- **Donors**: Donor profiles with blood type and donation history
- **Recipients**: Recipient information and request history
- **BloodInventory**: Current stock levels by blood type
- **Transactions**: Records of all blood donations and sales
- **Appointments**: Scheduled donation appointments

### Additional Documentation

For detailed technical documentation, please refer to:
- [API Documentation](./docs/api.md)
- [Database Schema](./prisma/schema.prisma)
- [Contribution Guidelines](./CONTRIBUTING.md)

## 8. Author & Contact

**Adnane Ahroum**

- GitHub: [@Adnane-Ahroum](https://github.com/Adnane-Ahroum)
- Email: adnane.ahroum@example.com
- LinkedIn: [Adnane Ahroum](https://linkedin.com/in/adnane-ahroum)

### Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Adnane-Ahroum/GoldenBlood/issues).

If you'd like to contribute:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 9. License

MIT License

Copyright (c) 2024 Adnane Ahroum

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## 10. Acknowledgements

- **Next.js Team** - For the incredible React framework
- **Prisma** - For the excellent ORM and database toolkit
- **Tailwind CSS** - For the utility-first CSS framework
- **Vercel** - For seamless deployment and hosting solutions
- **Open Source Community** - For the countless libraries and tools that made this project possible
- **Healthcare Professionals** - For their insights into blood management challenges
- **Beta Testers** - For their valuable feedback during development
- **Contributors** - Everyone who has contributed to improving GoldenBlood

---

⭐ If you find this project useful, please consider giving it a star on GitHub!

🩸 **Together, we can make blood donation more accessible and save lives.**
