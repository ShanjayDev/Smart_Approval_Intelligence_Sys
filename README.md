# Smart Approval Intelligence System

A modern, AI-powered approval management system with risk prediction, auto-approval rules, and comprehensive analytics.

## Features

✨ **Core Features:**
- 🔐 Secure user authentication (Login/Logout)
- 📊 Real-time analytics dashboard with approval statistics
- 📝 Request submission with AI-powered risk assessment
- 🤖 Rule-based auto-approval system
- 👥 Manager review queue for escalated requests
- 📈 Admin analytics with charts and reports
- 🔔 Real-time notifications for status updates
- 🎨 Modern, professional UI with responsive design

## Technology Stack

**Frontend:**
- React 18 with TypeScript
- TailwindCSS for styling
- React Router for navigation
- Axios for API calls
- Chart.js for analytics
- React Toastify for notifications

**Backend:**
- Node.js with Express
- MongoDB with Mongoose
- JWT for authentication
- AI/LLM integration for risk prediction
- RESTful API architecture

**Design:**
- Deep Blue Primary (#1e3a8a)
- Emerald for Approvals (#10b981)
- Amber for Pending (#f59e0b)
- Red for Rejections (#ef4444)

## Project Structure

```
smart-approval-intelligence/
├── backend/                 # Express API server
│   ├── src/
│   │   ├── models/         # MongoDB schemas
│   │   ├── routes/         # API endpoints
│   │   ├── controllers/    # Business logic
│   │   ├── middleware/     # Auth & validation
│   │   ├── utils/          # Utilities & AI service
│   │   └── server.ts       # Entry point
│   ├── .env.example
│   └── package.json
│
├── frontend/               # React application
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── services/       # API services
│   │   ├── hooks/          # Custom hooks
│   │   ├── types/          # TypeScript types
│   │   ├── styles/         # Global styles
│   │   ├── App.tsx         # Main app
│   │   └── index.tsx       # Entry point
│   ├── public/             # Static assets
│   └── package.json
│
├── package.json            # Root package manager
└── README.md
```

## Installation

### Option 1: Install All Dependencies at Once
```bash
npm run install-all
```

### Option 2: Manual Installation

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd frontend
npm install
```

## Environment Setup

### Backend (.env)
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/smart-approval
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
OPENAI_API_KEY=your_openai_api_key_here (or use local LLM)
```

### Frontend (.env)
```
REACT_APP_API_URL=http://localhost:5000
```

## Running the Application

### Development Mode - Start Both Backend and Frontend

```bash
npm start
```

Or start them separately:

**Terminal 1 - Backend:**
```bash
npm run start:backend
```

**Terminal 2 - Frontend:**
```bash
npm run start:frontend
```

- **Backend:** http://localhost:5000
- **Frontend:** http://localhost:3000

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/profile` - Get user profile

### Requests
- `GET /api/requests` - Get all requests
- `POST /api/requests` - Create new request
- `GET /api/requests/:id` - Get request details
- `PUT /api/requests/:id` - Update request
- `DELETE /api/requests/:id` - Delete request

### Review Queue
- `GET /api/review-queue` - Get pending reviews
- `POST /api/review-queue/:id/approve` - Approve request
- `POST /api/review-queue/:id/reject` - Reject request

### Analytics
- `GET /api/analytics/dashboard` - Dashboard stats
- `GET /api/analytics/requests` - Request analytics
- `GET /api/analytics/approvals` - Approval analytics

### AI Risk Assessment
- `POST /api/ai/assess-risk` - Assess request risk

## Default Login Credentials (Development)

- Email: `admin@example.com`
- Password: `admin123`

## Building for Production

```bash
npm run build
```

## Testing

```bash
npm test
```

## Features Documentation

### 1. Dashboard
- Overview of system statistics
- Recent request activity
- Approval rate metrics
- User engagement charts

### 2. Submit Request
- Form with field validation
- File attachments
- AI risk assessment
- Auto-approval eligibility check

### 3. My Requests
- User's all requests history
- Status tracking
- Filter and search
- Request details view

### 4. Review Queue
- Pending requests for managers
- Risk assessment details
- Approval/Rejection workflow
- Comment system

### 5. Analytics (Admin)
- Request statistics
- Approval trends
- Risk distribution
- User activity reports
- Export functionality



