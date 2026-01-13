# TeleCare: AI-Assisted System to Connect Rural Patients to Urban Doctors

## 🏥 Project Overview

**TeleCare** is a comprehensive telemedicine platform designed to bridge the healthcare accessibility gap between rural patients and urban doctors. This full-stack web application enables secure video consultations, AI-powered symptom analysis, prescription management, and multi-language support to serve India's diverse rural population.

## ✨ Key Features

### 🔐 Authentication & User Management
- **Firebase Authentication** with email/password
- **Multi-role system** (Patient, Doctor, Admin)
- **Protected routes** with role-based access control
- **User profiles** with detailed medical history
- **Password reset** functionality

### 🎥 Video Consultation System
- **Jitsi Meet Integration** for secure video calls
- **Real-time consultation rooms** with screen sharing
- **Chat during video calls** for better communication
- **File sharing** during consultations
- **Consultation history** and recordings

### 🤖 AI-Powered Medical Assistant
- **Google Gemini AI** integration for symptom analysis
- **Medical chatbot** with natural language processing
- **Intelligent symptom checker** with preliminary diagnosis
- **Medical advice** with disclaimer about professional consultation
- **Voice input support** for accessibility

### 📱 Multi-language Support
- **Internationalization (i18n)** with React i18next
- **Support for 3 languages**: English, Hindi, Telugu
- **Dynamic language switching** without page reload
- **Localized content** for all UI elements
- **Browser language detection**

### 📋 Appointment Management
- **Appointment booking** with calendar integration
- **Doctor availability** scheduling
- **Appointment status tracking** (Upcoming, Past, Cancelled)
- **Appointment reminders** and notifications
- **Rescheduling and cancellation** options

### 💊 Prescription Management
- **Digital prescriptions** creation and management
- **Prescription viewer** with detailed medication info
- **Prescription history** for patients
- **PDF generation** for prescription downloads
- **Drug interaction warnings**

### 📄 Document Management
- **Medical document upload** and storage
- **Firebase Storage** integration for secure file handling
- **Document categorization** (Lab reports, X-rays, etc.)
- **Document sharing** between patients and doctors
- **Version control** for updated documents

### 👨‍⚕️ Doctor Dashboard
- **Patient management** system
- **Appointment scheduling** and management
- **Patient medical history** access
- **Prescription creation** tools
- **Consultation notes** and follow-ups

### 📊 Analytics & Reporting
- **Firebase Analytics** integration
- **User engagement tracking**
- **Consultation metrics**
- **System performance monitoring**

## 🛠 Technology Stack

### Frontend
- **React 18.3.1** - Modern UI library
- **TypeScript 5.5.3** - Type safety and better development experience
- **Vite 5.4.1** - Fast build tool and development server
- **React Router DOM 6.26.2** - Client-side routing
- **TailwindCSS 3.4.11** - Utility-first CSS framework
- **shadcn/ui** - Modern UI component library built on Radix UI

### Backend
- **Node.js with Express 5.1.0** - RESTful API server
- **Firebase 11.6.0** - Authentication, Database, and Storage
- **Supabase 2.49.4** - Additional database and real-time features
- **Google Generative AI 0.24.1** - AI chatbot integration

### UI Components & Libraries
- **Radix UI** - Accessible UI primitives
  - Accordion, Alert Dialog, Avatar, Button, Calendar, Card, Checkbox, Dialog, Dropdown Menu, Form, Input, Label, Navigation Menu, Popover, Progress, Radio Group, Select, Slider, Switch, Tabs, Textarea, Toast, Tooltip
- **Lucide React 0.462.0** - Beautiful SVG icons
- **React Hook Form 7.53.0** - Form validation and management
- **Zod 3.23.8** - Schema validation
- **Date-fns 3.6.0** - Date manipulation utilities

### Video & Communication
- **Jitsi React SDK 1.4.4** - Video conferencing integration
- **WebRTC** - Real-time peer-to-peer communication

### Charts & Data Visualization
- **Recharts 2.12.7** - Composable charting library for React

### State Management & Data Fetching
- **TanStack React Query 5.56.2** - Server state management
- **Axios 1.8.4** - HTTP client for API calls

### Development Tools
- **ESLint 9.9.0** - Code linting
- **TypeScript ESLint 8.0.1** - TypeScript-specific linting
- **PostCSS 8.4.47** - CSS processing
- **Autoprefixer 10.4.20** - CSS vendor prefixing
- **Vite Plugin React SWC 3.5.0** - Fast React refresh

### Build & Deployment
- **Bun** - Fast package manager and runtime
- **Node.js 22.5.5** - Server runtime
- **CORS 2.8.5** - Cross-origin resource sharing
- **dotenv 17.2.3** - Environment variable management

## 📁 Project Structure

```
TeleCare-AI-Assisted-System/
├── app/                          # Next.js App Router (if applicable)
│   └── api/                      # API routes
│       └── chatbot/             # Chatbot API endpoint
├── public/                       # Static assets
│   └── robots.txt               # SEO robots file
├── src/                         # Main source code
│   ├── components/              # React components
│   │   ├── chat/               # Chat-related components
│   │   │   ├── FloatingChatButton.tsx
│   │   │   └── MedicalChatbot.tsx
│   │   ├── consultations/      # Video consultation components
│   │   │   └── VideoConsultation.tsx
│   │   ├── documents/          # Document management
│   │   │   └── DocumentUpload.tsx
│   │   ├── prescriptions/      # Prescription components
│   │   │   └── PrescriptionViewer.tsx
│   │   ├── ui/                 # Reusable UI components (shadcn/ui)
│   │   ├── Footer.tsx          # App footer
│   │   ├── LanguageSwitcher.tsx # Language selection
│   │   ├── Layout.tsx          # Main layout wrapper
│   │   ├── Navbar.tsx          # Navigation header
│   │   └── ProtectedRoute.tsx  # Route protection
│   ├── data/                   # Static data
│   │   └── doctors.ts          # Doctor information
│   ├── hooks/                  # Custom React hooks
│   │   ├── use-mobile.tsx      # Mobile device detection
│   │   └── use-toast.ts        # Toast notifications
│   ├── lib/                    # Utility libraries
│   │   ├── api.ts              # API client configuration
│   │   ├── auth-context.tsx    # Authentication context
│   │   ├── config.ts           # App configuration
│   │   ├── db-service.ts       # Database service layer
│   │   ├── firebase.ts         # Firebase configuration
│   │   ├── i18n.ts            # Internationalization setup
│   │   └── utils.ts           # Utility functions
│   ├── locales/               # Translation files
│   │   ├── en.json            # English translations
│   │   ├── hi.json            # Hindi translations
│   │   └── te.json            # Telugu translations
│   ├── pages/                 # Page components
│   │   ├── appointments/      # Appointment-related pages
│   │   ├── doctor/           # Doctor dashboard pages
│   │   ├── patients/         # Patient management pages
│   │   ├── Appointments.tsx   # Main appointments page
│   │   ├── ConsultationRoom.tsx # Video consultation page
│   │   ├── Consultations.tsx  # Consultations list
│   │   ├── Dashboard.tsx      # Main dashboard
│   │   ├── DoctorDashboard.tsx # Doctor-specific dashboard
│   │   ├── Doctors.tsx        # Doctors listing
│   │   ├── Documents.tsx      # Document management
│   │   ├── Features.tsx       # Platform features showcase
│   │   ├── ForgotPassword.tsx # Password reset
│   │   ├── Index.tsx          # Landing page
│   │   ├── Login.tsx          # User login
│   │   ├── MedicalChat.tsx    # AI chat interface
│   │   ├── Prescription.tsx   # Prescription management
│   │   ├── Settings.tsx       # User settings
│   │   └── Signup.tsx         # User registration
│   ├── types/                 # TypeScript type definitions
│   │   └── firebase.d.ts      # Firebase type declarations
│   ├── App.tsx               # Main app component
│   ├── main.tsx              # App entry point
│   └── index.css             # Global styles
├── server.js                 # Express.js backend server
├── package.json             # Dependencies and scripts
├── package-lock.json        # Dependency lock file
├── bun.lockb               # Bun package manager lock file
├── tsconfig.json           # TypeScript configuration
├── tsconfig.app.json       # TypeScript app configuration
├── tsconfig.node.json      # TypeScript Node.js configuration
├── vite.config.ts          # Vite build configuration
├── tailwind.config.ts      # TailwindCSS configuration
├── postcss.config.js       # PostCSS configuration
├── eslint.config.js        # ESLint configuration
├── components.json         # shadcn/ui components configuration
├── .env                    # Environment variables
├── .gitignore             # Git ignore rules
├── index.html             # HTML entry point
├── test-gemini.mjs        # Gemini AI testing script
└── README.md              # Original documentation
```

## 🚀 Getting Started

### Prerequisites
- **Node.js 18+** installed
- **npm** or **bun** package manager
- **Git** for version control

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/TeleCare-AI-Assisted-System.git
   cd TeleCare-AI-Assisted-System
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   bun install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   # Google Gemini AI API Key
   VITE_GEMINI_API_KEY=your_gemini_api_key_here
   GEMINI_API_KEY=your_gemini_api_key_here
   
   # Firebase Configuration
   VITE_FIREBASE_API_KEY=your_firebase_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
   VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
   VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
   VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
   VITE_FIREBASE_APP_ID=your_firebase_app_id
   VITE_FIREBASE_MEASUREMENT_ID=your_firebase_measurement_id
   
   # Supabase Configuration
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   
   # Server Configuration
   PORT=3001
   ```

4. **Start the development servers**
   
   **Frontend (in one terminal):**
   ```bash
   npm run dev
   ```
   This starts the Vite development server at `http://localhost:5173`
   
   **Backend (in another terminal):**
   ```bash
   node server.js
   ```
   This starts the Express server at `http://localhost:3001`

5. **Open the application**
   Navigate to `http://localhost:5173` in your browser

## 📋 Available Scripts

- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run build:dev` - Build in development mode
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🔧 Configuration Files

- **`vite.config.ts`** - Vite build configuration with React plugin
- **`tailwind.config.ts`** - TailwindCSS configuration with custom theme
- **`tsconfig.json`** - TypeScript compiler configuration
- **`eslint.config.js`** - ESLint rules and configuration
- **`components.json`** - shadcn/ui components configuration

## 🌐 API Endpoints

### Backend Server (Express.js)
- `POST /api/chatbot` - Medical AI chatbot interaction
- Authentication endpoints (Firebase)
- File upload endpoints (Firebase Storage)

## 🔒 Security Features

- **Firebase Authentication** with secure token-based auth
- **Protected routes** with role-based access control
- **CORS** configuration for API security
- **Input validation** with Zod schemas
- **Sanitized AI responses** for medical safety

## 🌍 Internationalization

The app supports multiple languages through React i18next:
- **English (en)** - Default language
- **Hindi (hi)** - For Hindi-speaking users
- **Telugu (te)** - For Telugu-speaking users

Language files are located in `src/locales/` and can be extended for additional languages.

## 🎨 UI/UX Design

- **Responsive design** for mobile, tablet, and desktop
- **Dark/Light theme** support with next-themes
- **Accessible components** built with Radix UI
- **Modern design system** with consistent spacing and typography
- **Loading states** and error handling throughout the app

## 📱 Mobile Features

- **Responsive video calls** that work on mobile devices
- **Touch-friendly interface** for easy navigation
- **Mobile-optimized chat** interface
- **File upload** from mobile devices

## 🔮 Future Enhancements

- [ ] **Push notifications** for appointment reminders
- [ ] **Offline support** for basic features
- [ ] **Advanced AI diagnostics** with image analysis
- [ ] **Integration with wearable devices**
- [ ] **Pharmacy integration** for prescription fulfillment
- [ ] **Insurance claim processing**
- [ ] **Multi-provider video conferencing** options
- [ ] **Advanced analytics dashboard**

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Firebase** for authentication and storage services
- **Google Gemini AI** for intelligent medical assistance
- **Jitsi** for video conferencing capabilities
- **shadcn/ui** for beautiful and accessible UI components
- **Radix UI** for primitive UI components
- **The open-source community** for amazing tools and libraries

## 📞 Support

For support, email your-email@example.com or join our Slack channel.

---

**TeleCare** - Connecting Rural Healthcare to Urban Expertise through Technology ❤️