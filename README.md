# DataNomics AI Classroom Assistant

**Empowering Decisions through Data**

A production-grade, real-time AI-powered classroom teaching support system for African secondary schools.

## 🎯 Overview

DataNomics AI Classroom Assistant is a comprehensive platform designed to support teachers during live classroom instruction. Built with enterprise-grade architecture, it provides real-time AI assistance, automated question generation, student confusion detection, and comprehensive analytics.

### Contact Information

- **Email**: oburustephen@icloud.com
- **WhatsApp**: +254788122988
- **Phone**: +254701200233

## ✨ Core Features

### 1. Real-Time AI Teacher Copilot
- Instant concept explanations
- Dynamic example generation
- Concept simplification
- Activity creation
- Real-time quiz generation
- Voice input support
- Streaming AI responses

### 2. AI Question Generator
- Multiple choice questions
- Short answer questions
- Essay questions
- Auto-grading
- Bloom's taxonomy tagging
- Difficulty level assessment

### 3. Student Confusion Detection
- Real-time engagement analytics
- Wrong answer pattern recognition
- Response time analysis
- Participation tracking
- Automated intervention alerts
- Weak topic identification

### 4. Classroom Analytics Dashboard
- Engagement scoring
- Student performance metrics
- Topic mastery tracking
- Participation charts
- Attendance trends
- Performance comparisons

### 5. Lesson Simplification Engine
- AI-powered concept rewriting
- Local language analogies
- Beginner-friendly summaries
- Multiple reading levels

### 6. Offline-First Architecture
- Service worker caching
- Local data synchronization
- Low-bandwidth optimization
- Automatic sync queuing
- Resilient offline mode

### 7. Multi-Channel Communication
- **WhatsApp Integration**: Direct AI assistant
- **SMS Support**: Africa's Talking integration
- **Voice Support**: Twilio voice API
- **Web Platform**: Real-time web interface

### 8. Payment Integration
- **M-Pesa STK Push** (Kenya)
- **MTN MoMo API** (Uganda)
- **Stripe** (Global fallback)
- Subscription management
- Invoice generation

### 9. Role-Based Access Control
- Teachers
- Students
- School Administrators
- District Education Officers
- Ministry Analysts

### 10. Multi-Level Dashboards
- Teacher Dashboard
- School Dashboard
- District Dashboard
- Ministry Analytics Portal

## 🏗️ Architecture

### Frontend
- **Framework**: Next.js 15 with React
- **Styling**: Tailwind CSS
- **Animation**: Framer Motion
- **Language**: TypeScript
- **Real-time**: Socket.IO client
- **Offline**: Service Workers + IndexedDB

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Real-time**: Socket.IO
- **Authentication**: JWT + Role-based access
- **API**: RESTful + WebSocket

### Database
- **Primary**: PostgreSQL
- **ORM**: Prisma
- **Caching**: Redis
- **File Storage**: AWS S3 / Local

### AI Integration
- **Provider**: OpenAI API (GPT-4.1)
- **Streaming**: Server-sent events
- **Prompt Engineering**: Template-based system
- **Context Management**: Session-aware

### Deployment
- **Containerization**: Docker
- **Frontend**: Vercel
- **Backend**: Railway/Render
- **Database**: Managed PostgreSQL
- **CDN**: Cloudflare

## 📋 Tech Stack

### Core Dependencies

**Frontend**
```json
{
  "next": "15.x",
  "react": "19.x",
  "typescript": "5.x",
  "tailwindcss": "3.x",
  "framer-motion": "11.x",
  "socket.io-client": "4.x",
  "zustand": "4.x",
  "axios": "1.x",
  "react-hook-form": "7.x",
  "zod": "3.x"
}
```

**Backend**
```json
{
  "express": "4.x",
  "socket.io": "4.x",
  "prisma": "5.x",
  "@prisma/client": "5.x",
  "jsonwebtoken": "9.x",
  "bcryptjs": "2.x",
  "dotenv": "16.x",
  "cors": "2.x",
  "helmet": "7.x",
  "express-rate-limit": "7.x",
  "openai": "4.x",
  "twilio": "4.x",
  "stripe": "14.x",
  "node-cache": "5.x"
}
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18.x or higher
- PostgreSQL 14.x or higher
- Docker & Docker Compose
- Git
- npm or yarn

### Development Setup

```bash
# Clone repository
git clone https://github.com/oburustephen-lgtm/datanomics-ai-classroom.git
cd datanomics-ai-classroom

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env.local

# Generate Prisma Client
cd backend
npx prisma generate

# Run database migrations
npx prisma migrate dev

# Seed database (optional)
node scripts/seed.js

# Start development servers
cd ..
npm run dev
```

### Environment Variables

See `.env.example` for comprehensive configuration.

### Key Environment Variables

```bash
# Frontend
NEXT_PUBLIC_API_URL=http://localhost:3001
NEXT_PUBLIC_WS_URL=ws://localhost:3001

# Backend
DATABASE_URL=postgresql://user:password@localhost:5432/datanomics
JWT_SECRET=your_super_secret_jwt_key
OPENAI_API_KEY=sk-...

# Payments
STRIPE_SECRET_KEY=sk_test_...
MPESA_CONSUMER_KEY=...
MTN_MOMO_API_KEY=...

# Communications
TWILIO_ACCOUNT_SID=...
TWILIO_AUTH_TOKEN=...
AFRICAS_TALKING_API_KEY=...
WHATSAPP_BUSINESS_ACCOUNT_ID=...
```

## 📁 Project Structure

```
datanomics-ai-classroom/
├── frontend/
│   ├── app/
│   │   ├── (auth)/
│   │   ├── dashboard/
│   │   ├── classroom/
│   │   ├── analytics/
│   │   └── settings/
│   ├── components/
│   │   ├── ui/
│   │   ├── dashboard/
│   │   ├── classroom/
│   │   └── analytics/
│   ├── lib/
│   │   ├── api/
│   │   ├── socket/
│   │   ├── ai/
│   │   ├── offline/
│   │   └── utils/
│   ├── hooks/
│   ├── types/
│   ├── styles/
│   └── public/
├── backend/
│   ├── src/
│   │   ├── routes/
│   │   │   ├── auth.ts
│   │   │   ├── classroom.ts
│   │   │   ├── analytics.ts
│   │   │   ├── payments.ts
│   │   │   ├── ai.ts
│   │   │   └── communications.ts
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── services/
│   │   │   ├── ai/
│   │   │   ├── payment/
│   │   │   ├── communication/
│   │   │   └── analytics/
│   │   ├── utils/
│   │   ├── types/
│   │   ├── config/
│   │   ├── socket/
│   │   └── app.ts
│   ├── prisma/
│   │   ├── schema.prisma
│   │   └── migrations/
│   ├── scripts/
│   │   ├── seed.js
│   │   └── migrate.js
│   └── Dockerfile
├── docker-compose.yml
├── .env.example
└── README.md
```

## 🔐 Security Features

- **JWT Authentication**: Secure token-based auth
- **Role-Based Access Control**: Fine-grained permissions
- **Rate Limiting**: API rate limiting per user
- **CORS Protection**: Configured CORS headers
- **Helmet Security**: HTTP security headers
- **Input Validation**: Zod schema validation
- **SQL Injection Prevention**: Prisma ORM protection
- **API Key Management**: Secure API key storage
- **Audit Logging**: Comprehensive activity logging
- **Payment PCI Compliance**: Secure payment handling

## 📊 Database Schema

Full Prisma schema with:
- User management
- School & institution hierarchy
- Classroom sessions
- Lesson content
- Student performance
- AI interactions
- Payment records
- Analytics events
- Alerts & notifications

## 🤖 AI Integration

### Prompt Templates

- **Explanation Engine**: Concept clarification
- **Simplification Module**: Complex-to-simple conversion
- **Question Generator**: Multi-format question creation
- **Activity Designer**: Classroom activity generation
- **Intervention Suggester**: Personalized learning recommendations

### Features

- Streaming responses
- Context-aware replies
- Subject expertise integration
- Grade level adaptation
- Local language support

## 💳 Payment Integration

### M-Pesa (Kenya)

```typescript
// STK Push implementation
// Auto-payment prompts on user phones
```

### MTN MoMo (Uganda)

```typescript
// MoMo API integration
// Subscription processing
```

### Stripe (Global)

```typescript
// Card payments
// Subscription management
```

## 📱 Multi-Channel Communication

### WhatsApp AI Assistant
- Direct AI queries
- Lesson support
- Assignment submission

### SMS Gateway
- Africa's Talking integration
- Alert notifications
- Confirmation messages

### Voice Support
- Twilio voice API
- IVR system
- Voice lessons

## 🌐 Offline Support

### Implementation
- Service Worker caching
- IndexedDB storage
- Sync queue management
- Progressive enhancement
- Bandwidth optimization

## 📈 Analytics

### Teacher Analytics
- Class engagement
- Student performance
- Question effectiveness
- Time tracking

### School Analytics
- Teacher performance
- School benchmarks
- Subject mastery
- Attendance trends

### District Analytics
- Regional performance
- School comparisons
- Resource allocation
- Ministry reports

## 🎨 UI/UX Design

### Design System
- **Color Palette**: Blue (#0066CC) + Teal (#00B4D8) + White (#FFFFFF)
- **Typography**: Professional, readable fonts
- **Components**: Reusable, accessible components
- **Animation**: Smooth, purposeful transitions
- **Responsive**: Mobile-first design

### Dashboards
- Elegant, ministry-grade interfaces
- Real-time data updates
- Intuitive navigation
- Accessible (WCAG 2.1 AA)

## 🚢 Deployment

### Docker

```bash
docker-compose up -d
```

### Vercel (Frontend)

```bash
npm install -g vercel
vercel deploy
```

### Railway/Render (Backend)

See deployment guide.

### Database

Managed PostgreSQL on:
- Supabase
- Railway
- AWS RDS

## 📚 API Documentation

### Authentication

```bash
POST /api/auth/register
POST /api/auth/login
POST /api/auth/refresh
POST /api/auth/logout
```

### Classroom

```bash
GET /api/classroom/sessions
POST /api/classroom/sessions
WS /ws/classroom/:sessionId
```

### AI Assistance

```bash
POST /api/ai/explain
POST /api/ai/simplify
POST /api/ai/generate-questions
POST /api/ai/suggest-activities
```

### Analytics

```bash
GET /api/analytics/classroom
GET /api/analytics/school
GET /api/analytics/district
```

### Payments

```bash
POST /api/payments/initiate
POST /api/payments/callback
GET /api/payments/status
```

## 🧪 Testing

```bash
# Run tests
npm test

# Run with coverage
npm run test:coverage

# E2E tests
npm run test:e2e
```

## 📖 Documentation

- [Deployment Guide](./docs/DEPLOYMENT.md)
- [API Reference](./docs/API.md)
- [AI Integration Guide](./docs/AI.md)
- [Payment Integration](./docs/PAYMENTS.md)
- [Security Guide](./docs/SECURITY.md)
- [Architecture](./docs/ARCHITECTURE.md)

## 🤝 Contributing

1. Create feature branch
2. Commit changes
3. Push to branch
4. Create Pull Request

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Support

For support, contact:
- **Email**: oburustephen@icloud.com
- **WhatsApp**: +254788122988
- **Phone**: +254701200233

---

**DataNomics AI Classroom Assistant**
*Empowering Decisions through Data*
