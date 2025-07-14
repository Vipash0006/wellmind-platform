<div align="center">

# 🧠 WellMind
### *Mental Health, Redefined*

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.0-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://mongodb.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

![WellMind Dashboard](./frontend/public/readme_img.png)

*A modern, secure, and intuitive web platform connecting patients with licensed therapists for seamless mental health services*

</div>

---

## 📋 Table of Contents

- [🌟 Overview](#-overview)
- [✨ Features](#-features)
- [🏗️ System Architecture](#️-system-architecture)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Quick Start](#-quick-start)
- [📁 Project Structure](#-project-structure)
- [🔧 API Documentation](#-api-documentation)
- [🎯 User Journey](#-user-journey)
- [🌐 Deployment](#-deployment)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🌟 Overview

**WellMind** is a comprehensive mental health platform designed to bridge the gap between patients seeking mental health support and qualified therapists. Built with modern web technologies, it offers a secure, scalable, and user-friendly experience for all stakeholders.

> 💡 **Mission**: Making mental health care accessible, affordable, and efficient for everyone.

### 🎯 Key Goals
- **Accessibility**: Easy-to-use interface for all age groups
- **Security**: HIPAA-compliant data handling and privacy
- **Scalability**: Built to handle thousands of concurrent users
- **Efficiency**: Streamlined booking and management processes

---

## ✨ Features

```mermaid
mindmap
  root((WellMind Features))
    User Management
      🔐 Secure Authentication
      👤 Profile Management
      📊 Dashboard Analytics
    Therapist Services
      🔍 Advanced Search & Filtering
      📅 Real-time Availability
      ⭐ Reviews & Ratings
      💬 Specialization Tags
    Appointment System
      📱 Easy Booking Interface
      🔔 Smart Notifications
      📋 Medical History
      💳 Payment Integration
    Admin Panel
      👨‍⚕️ Therapist Management
      📈 Analytics & Reports
      🛠️ System Configuration
      💰 Revenue Tracking
```

### 🔐 **Authentication & Security**
- Multi-role authentication (Patient, Therapist, Admin)
- JWT-based secure session management
- Password encryption with bcrypt
- Protected routes and API endpoints

### 👨‍⚕️ **Therapist Management**
- Comprehensive therapist profiles
- Specialization and certification tracking
- Availability calendar management
- Performance analytics

### 📅 **Appointment System**
- Real-time booking with conflict prevention
- Automated email/SMS notifications
- Appointment history and medical records
- Cancellation and rescheduling options

### 📊 **Analytics Dashboard**
- User engagement metrics
- Revenue and performance tracking
- Appointment statistics
- Therapist productivity insights

---

## 🏗️ System Architecture

```mermaid
graph TB
    subgraph "Client Layer"
        A[Patient Portal<br/>React + Vite]
        B[Admin Dashboard<br/>React + Vite]
        C[Mobile App<br/>Future Implementation]
    end
    
    subgraph "API Gateway"
        D[Express.js Server<br/>Port 5000]
    end
    
    subgraph "Authentication"
        E[JWT Middleware]
        F[Role-based Access Control]
    end
    
    subgraph "Business Logic"
        G[User Controller]
        H[Therapist Controller]
        I[Admin Controller]
        J[Appointment Controller]
    end
    
    subgraph "Data Layer"
        K[(MongoDB Atlas<br/>Primary Database)]
        L[Cloudinary<br/>Media Storage]
        M[Redis Cache<br/>Future Implementation]
    end
    
    A --> D
    B --> D
    C --> D
    D --> E
    E --> F
    F --> G
    F --> H
    F --> I
    F --> J
    G --> K
    H --> K
    I --> K
    J --> K
    G --> L
    H --> L
```

---

## 🛠️ Tech Stack

<div align="center">

### Frontend Technologies
| Technology | Version | Purpose |
|------------|---------|---------|
| ![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=flat-square&logo=react) | 18.2.0 | UI Framework |
| ![Vite](https://img.shields.io/badge/Vite-4.x-646CFF?style=flat-square&logo=vite) | 4.x | Build Tool |
| ![Tailwind](https://img.shields.io/badge/Tailwind-3.x-06B6D4?style=flat-square&logo=tailwind-css) | 3.x | CSS Framework |
| ![React Router](https://img.shields.io/badge/React_Router-6.x-CA4245?style=flat-square&logo=react-router) | 6.x | Routing |

### Backend Technologies
| Technology | Version | Purpose |
|------------|---------|---------|
| ![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?style=flat-square&logo=node.js) | 18.x | Runtime Environment |
| ![Express](https://img.shields.io/badge/Express-4.x-000000?style=flat-square&logo=express) | 4.x | Web Framework |
| ![MongoDB](https://img.shields.io/badge/MongoDB-6.0-47A248?style=flat-square&logo=mongodb) | 6.0 | Database |
| ![Mongoose](https://img.shields.io/badge/Mongoose-7.x-880000?style=flat-square) | 7.x | ODM |

### DevOps & Deployment
| Technology | Purpose |
|------------|---------|
| ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws) | Cloud Hosting |
| ![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary) | Media Management |
| ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=json-web-tokens) | Authentication |

</div>

---

## 🚀 Quick Start

### 📋 Prerequisites

```bash
# Required Software
Node.js >= 18.0.0
npm >= 8.0.0
Git >= 2.30.0
MongoDB >= 6.0 (Local or Atlas)
```

### ⚡ Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/wellmind.git
cd wellmind

# 2️⃣ Install dependencies for all modules
npm run install-all
# OR manually:
cd backend && npm install
cd ../frontend && npm install  
cd ../admin && npm install
```

### 🔧 Environment Configuration

Create environment files in each directory:

<details>
<summary>📁 <strong>Backend Environment (.env)</strong></summary>

```bash
# Server Configuration
PORT=5000
NODE_ENV=development

# Database
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/wellmind
DB_NAME=wellmind

# Authentication
JWT_SECRET=your-super-secret-jwt-key-here
JWT_EXPIRE=7d

# Cloudinary Configuration
CLOUDINARY_CLOUD_NAME=your-cloud-name
CLOUDINARY_API_KEY=your-api-key
CLOUDINARY_API_SECRET=your-api-secret

# Email Configuration (Optional)
EMAIL_SERVICE=gmail
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password

# Payment Gateway (Future)
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
```

</details>

<details>
<summary>📁 <strong>Frontend Environment (.env)</strong></summary>

```bash
# API Configuration
VITE_BACKEND_URL=http://localhost:5000
VITE_API_VERSION=v1

# App Configuration
VITE_APP_NAME=WellMind
VITE_APP_VERSION=1.0.0

# External Services
VITE_GOOGLE_MAPS_API_KEY=your-maps-api-key
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_...
```

</details>

<details>
<summary>📁 <strong>Admin Environment (.env)</strong></summary>

```bash
# API Configuration
VITE_BACKEND_URL=http://localhost:5000
VITE_API_VERSION=v1

# Admin Configuration
VITE_ADMIN_APP_NAME=WellMind Admin
VITE_ADMIN_VERSION=1.0.0
```

</details>

### 🎬 Running the Application

```bash
# 🚀 Start all services concurrently
npm run dev

# OR start individually:

# 1️⃣ Start Backend Server
cd backend
npm run dev
# Server running on http://localhost:5000

# 2️⃣ Start Frontend Application  
cd frontend
npm run dev
# App running on http://localhost:5173

# 3️⃣ Start Admin Dashboard
cd admin  
npm run dev
# Admin panel on http://localhost:5174
```

### 🎯 Default Access URLs

| Service | URL | Description |
|---------|-----|-------------|
| 🌐 **Frontend** | http://localhost:5173 | Patient Portal |
| ⚙️ **Admin** | http://localhost:5174 | Admin Dashboard |
| 🔧 **API** | http://localhost:5000 | Backend API |
| 📚 **API Docs** | http://localhost:5000/api-docs | Swagger Documentation |

---

## 📁 Project Structure

```mermaid
graph TD
    A[WellMind Root] --> B[📁 backend/]
    A --> C[📁 frontend/]
    A --> D[📁 admin/]
    A --> E[📄 README.md]
    A --> F[📄 package.json]
    
    B --> B1[📁 config/]
    B --> B2[📁 controllers/]
    B --> B3[📁 middleware/]
    B --> B4[📁 models/]
    B --> B5[📁 routes/]
    B --> B6[📄 index.js]
    
    C --> C1[📁 src/]
    C --> C2[📁 public/]
    C --> C3[📄 package.json]
    
    D --> D1[📁 src/]
    D --> D2[📁 public/]
    D --> D3[📄 package.json]
    
    C1 --> C11[📁 components/]
    C1 --> C12[📁 pages/]
    C1 --> C13[📁 context/]
    C1 --> C14[📁 assets/]
    C1 --> C15[📄 App.jsx]
    
    D1 --> D11[📁 components/]
    D1 --> D12[📁 pages/]
    D1 --> D13[📁 context/]
    D1 --> D14[📁 assets/]
    D1 --> D15[📄 App.jsx]
```

<details>
<summary>📂 <strong>Detailed Directory Structure</strong></summary>

```
wellmind/
├── 📁 backend/                 # Node.js API Server
│   ├── 📁 config/             # Configuration files
│   │   ├── 📄 mongodb.js      # Database connection
│   │   └── 📄 cloudinary.js   # Media storage config
│   ├── 📁 controllers/        # Business logic
│   │   ├── 📄 userController.js
│   │   ├── 📄 therapistController.js
│   │   └── 📄 adminController.js
│   ├── 📁 middleware/         # Express middleware
│   │   ├── 📄 authUser.js     # User authentication
│   │   ├── 📄 authTherapist.js # Therapist auth
│   │   ├── 📄 authAdmin.js    # Admin authentication
│   │   └── 📄 multer.js       # File upload handling
│   ├── 📁 models/             # Database schemas
│   │   ├── 📄 userModel.js    # Patient model
│   │   ├── 📄 therapistModel.js # Therapist model
│   │   └── 📄 appointmentModel.js # Appointment model
│   ├── 📁 routes/             # API endpoints
│   │   ├── 📄 userRoutes.js   # Patient routes
│   │   ├── 📄 therapistRoutes.js # Therapist routes
│   │   └── 📄 adminRoutes.js  # Admin routes
│   ├── 📄 index.js            # Server entry point
│   └── 📄 package.json        # Dependencies
│
├── 📁 frontend/               # React Patient Portal
│   ├── 📁 public/            # Static assets
│   ├── 📁 src/               # Source code
│   │   ├── 📁 components/    # Reusable components
│   │   │   ├── 📄 Header.jsx
│   │   │   ├── 📄 Footer.jsx
│   │   │   ├── 📄 Navbar.jsx
│   │   │   └── 📄 SpecialityMenu.jsx
│   │   ├── 📁 pages/         # Page components
│   │   │   ├── 📄 Home.jsx
│   │   │   ├── 📄 Login.jsx
│   │   │   ├── 📄 Therapists.jsx
│   │   │   ├── 📄 Appointment.jsx
│   │   │   └── 📄 MyProfile.jsx
│   │   ├── 📁 context/       # State management
│   │   │   └── 📄 AppContext.jsx
│   │   ├── 📁 assets/        # Images, icons, styles
│   │   ├── 📄 App.jsx        # Main app component
│   │   └── 📄 main.jsx       # Entry point
│   └── 📄 package.json
│
└── 📁 admin/                  # React Admin Dashboard
    ├── 📁 public/            # Static assets
    ├── 📁 src/               # Source code
    │   ├── 📁 components/    # Admin components
    │   │   ├── 📄 Navbar.jsx
    │   │   └── 📄 Sidebar.jsx
    │   ├── 📁 pages/         # Admin pages
    │   │   ├── 📄 Dashboard.jsx
    │   │   ├── 📄 AddTherapist.jsx
    │   │   ├── 📄 TherapistList.jsx
    │   │   └── 📄 AllAppointments.jsx
    │   ├── 📁 context/       # Admin state management
    │   │   ├── 📄 AdminContext.jsx
    │   │   └── 📄 TherapistContext.jsx
    │   ├── 📄 App.jsx
    │   └── 📄 main.jsx
    └── 📄 package.json
```

</details>

---

## 🔧 API Documentation

### 🔐 Authentication Endpoints

```mermaid
sequenceDiagram
    participant C as Client
    participant S as Server
    participant DB as Database
    
    C->>S: POST /api/auth/register
    S->>DB: Create user account
    DB-->>S: User created
    S-->>C: JWT token + user data
    
    C->>S: POST /api/auth/login
    S->>DB: Verify credentials
    DB-->>S: User verified
    S-->>C: JWT token + user data
    
    C->>S: GET /api/auth/profile (with JWT)
    S->>DB: Get user profile
    DB-->>S: User profile data
    S-->>C: Profile information
```

### 📊 API Endpoints Overview

<details>
<summary>👤 <strong>User/Patient Endpoints</strong></summary>

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/api/auth/register` | Register new patient | ❌ |
| `POST` | `/api/auth/login` | Patient login | ❌ |
| `GET` | `/api/user/profile` | Get patient profile | ✅ |
| `PUT` | `/api/user/profile` | Update patient profile | ✅ |
| `GET` | `/api/user/appointments` | Get patient appointments | ✅ |
| `POST` | `/api/user/book-appointment` | Book new appointment | ✅ |
| `PUT` | `/api/user/cancel-appointment/:id` | Cancel appointment | ✅ |

</details>

<details>
<summary>👨‍⚕️ <strong>Therapist Endpoints</strong></summary>

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/api/therapist/login` | Therapist login | ❌ |
| `GET` | `/api/therapist/profile` | Get therapist profile | ✅ |
| `PUT` | `/api/therapist/profile` | Update profile | ✅ |
| `GET` | `/api/therapist/appointments` | Get therapist appointments | ✅ |
| `PUT` | `/api/therapist/appointment/:id` | Update appointment status | ✅ |
| `GET` | `/api/therapist/earnings` | Get earnings data | ✅ |
| `PUT` | `/api/therapist/availability` | Set availability | ✅ |

</details>

<details>
<summary>⚙️ <strong>Admin Endpoints</strong></summary>

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `POST` | `/api/admin/login` | Admin login | ❌ |
| `GET` | `/api/admin/dashboard` | Get dashboard stats | ✅ |
| `POST` | `/api/admin/add-therapist` | Add new therapist | ✅ |
| `GET` | `/api/admin/therapists` | Get all therapists | ✅ |
| `PUT` | `/api/admin/therapist/:id` | Update therapist | ✅ |
| `DELETE` | `/api/admin/therapist/:id` | Remove therapist | ✅ |
| `GET` | `/api/admin/appointments` | Get all appointments | ✅ |
| `GET` | `/api/admin/analytics` | Get system analytics | ✅ |

</details>

---

## 🎯 User Journey

```mermaid
journey
    title Patient Appointment Booking Journey
    section Discovery
      Visit website: 5: Patient
      Browse therapists: 4: Patient
      Read reviews: 4: Patient
    section Registration
      Create account: 3: Patient
      Verify email: 3: Patient
      Complete profile: 4: Patient
    section Booking
      Search therapists: 5: Patient
      View availability: 5: Patient
      Select time slot: 5: Patient
      Make payment: 4: Patient
      Receive confirmation: 5: Patient
    section Appointment
      Attend session: 5: Patient, Therapist
      Provide feedback: 4: Patient
      Book follow-up: 4: Patient
```

### 🔄 Application Flow

```mermaid
graph LR
    A[🏠 Landing Page] --> B{👤 User Type?}
    B -->|Patient| C[📝 Patient Registration]
    B -->|Therapist| D[🔐 Therapist Login]
    B -->|Admin| E[⚙️ Admin Login]
    
    C --> F[📋 Complete Profile]
    F --> G[🔍 Browse Therapists]
    G --> H[📅 Book Appointment]
    H --> I[💳 Payment]
    I --> J[✅ Confirmation]
    
    D --> K[👨‍⚕️ Therapist Dashboard]
    K --> L[📊 View Appointments]
    K --> M[💰 Track Earnings]
    
    E --> N[📈 Admin Dashboard]
    N --> O[👥 Manage Therapists]
    N --> P[📊 View Analytics]
```

---

## 🌐 Deployment

### ☁️ Cloud Architecture

```mermaid
graph TB
    subgraph "AWS Cloud Infrastructure"
        subgraph "Frontend Deployment"
            A[AWS Amplify<br/>React Apps]
            A1[Patient Portal<br/>wellmind.com]
            A2[Admin Dashboard<br/>admin.wellmind.com]
        end
        
        subgraph "Backend Services"
            B[AWS EC2<br/>Node.js API]
            C[Application Load Balancer]
            D[Auto Scaling Group]
        end
        
        subgraph "Database & Storage"
            E[(MongoDB Atlas<br/>Primary Database)]
            F[Cloudinary<br/>Media Storage]
            G[AWS S3<br/>Backup Storage]
        end
        
        subgraph "Security & Monitoring"
            H[AWS CloudFront<br/>CDN]
            I[AWS WAF<br/>Web Application Firewall]
            J[CloudWatch<br/>Monitoring]
        end
    end
    
    Users --> H
    H --> A
    A --> A1
    A --> A2
    A1 --> C
    A2 --> C
    C --> B
    B --> D
    B --> E
    B --> F
    B --> G
    J --> B
    I --> C
```

### 🚀 Deployment Scripts

<details>
<summary>📜 <strong>Production Deployment</strong></summary>

```bash
#!/bin/bash
# deploy.sh - Production deployment script

# Build frontend applications
echo "🏗️ Building frontend applications..."
cd frontend && npm run build
cd ../admin && npm run build

# Deploy to AWS Amplify
echo "🚀 Deploying to AWS Amplify..."
aws amplify start-deployment --app-id $AMPLIFY_APP_ID

# Deploy backend to EC2
echo "🔧 Deploying backend to EC2..."
rsync -avz --exclude node_modules backend/ $EC2_USER@$EC2_HOST:/var/www/wellmind/

# Restart services
echo "♻️ Restarting services..."
ssh $EC2_USER@$EC2_HOST "pm2 restart wellmind-api"

echo "✅ Deployment completed successfully!"
```

</details>

### 📊 Environment Configuration

| Environment | Frontend URL | Backend URL | Database |
|-------------|--------------|-------------|----------|
| 🧪 **Development** | http://localhost:5173 | http://localhost:5000 | Local MongoDB |
| 🎭 **Staging** | https://staging.wellmind.com | https://api-staging.wellmind.com | MongoDB Atlas (Test) |
| 🚀 **Production** | https://wellmind.com | https://api.wellmind.com | MongoDB Atlas (Prod) |

---

## 🤝 Contributing

We welcome contributions! Please see our contribution guidelines below:

### 🔄 Development Workflow

```mermaid
gitgraph
    commit id: "Initial commit"
    branch develop
    checkout develop
    commit id: "Add feature branch"
    branch feature/user-authentication
    checkout feature/user-authentication
    commit id: "Implement JWT auth"
    commit id: "Add password validation"
    checkout develop
    merge feature/user-authentication
    commit id: "Feature merged"
    checkout main
    merge develop
    commit id: "Release v1.0.0"
```

### 📝 Contribution Steps

1. **Fork the repository**
   ```bash
   git clone https://github.com/yourusername/wellmind.git
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make your changes**
   - Follow our coding standards
   - Add tests for new features
   - Update documentation

4. **Commit your changes**
   ```bash
   git commit -m "✨ Add amazing feature"
   ```

5. **Push to your branch**
   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open a Pull Request**

### 🎯 Development Guidelines

- ✅ Follow ESLint and Prettier configurations
- ✅ Write meaningful commit messages
- ✅ Add tests for new features
- ✅ Update documentation
- ✅ Ensure responsive design
- ✅ Follow accessibility guidelines

---

<div align="center">

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

Built with ❤️ by the WellMind Team

[![Made with React](https://img.shields.io/badge/Made%20with-React-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![Powered by Node.js](https://img.shields.io/badge/Powered%20by-Node.js-339933?style=for-the-badge&logo=node.js)](https://nodejs.org/)
[![Database MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb)](https://mongodb.com/)

**Made with 💙 for better mental health**

---

*© 2025 WellMind. All rights reserved.*

</div>

