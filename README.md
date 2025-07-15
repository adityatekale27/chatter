# Chatter

A modern, full-stack real-time chat application built with Next.js, TypeScript, and MongoDB. Features instant messaging, video calling, friend systems, and a responsive design optimised for both desktop and mobile devices.

## 🚀 Features

### Core Functionality
- **Real-Time Messaging**: Instant one-to-one and group conversations
- **Video & Audio Calling**: WebRTC-powered peer-to-peer communication
- **Friend System**: Send/receive friend requests and manage connections
- **User Authentication**: Secure login and registration with NextAuth.js
- **Responsive Design**: Seamless experience across all devices

### Advanced Features
- **Message Status**: Delivery and read receipts for all messages
- **Real-Time Notifications**: Instant alerts for new messages and friend requests
- **Online/Offline Indicators**: See when friends are available
- **Infinite Scroll**: Smooth message history loading
- **User Search**: Find and connect with other users
- **Rate Limiting**: Protection against spam and abuse
- **Session Management**: Secure user sessions and authentication

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **React 19** - Latest React with enhanced performance
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **React Hook Forms** - Performant forms with easy validation

### Backend
- **Next.js API Routes** - Serverless API endpoints
- **Prisma ORM** - Type-safe database toolkit
- **MongoDB** - NoSQL database with Prisma adapter
- **NextAuth.js** - Authentication solution
- **Bcrypt.js** - Password hashing and security

### Real-Time & Communication
- **Pusher** - Real-time messaging infrastructure
- **WebRTC** - Peer-to-peer video/audio calling

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ (Required for Next.js 15)
- MongoDB Atlas account or local MongoDB instance
- Pusher account for real-time messaging
- Cloudinary account for image/media uploads
- NextAuth.js providers (Google, GitHub, etc.)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/adityatekale27/chatter.git
cd chatter
```

2. **Install dependencies**
```bash
npm install
# or
yarn install
```

3. **Environment Setup**
Create a `.env` file in the root directory:
```env
NODE_ENV="development"

# Database
DATABASE_URL="mongodb+srv://username:password@cluster.mongodb.net/chatter"

# NextAuth
NEXTAUTH_SECRET="your-nextauth-secret"
NEXTAUTH_URL="http://localhost:3000"

# OAuth Providers
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
GITHUB_CLIENT_ID="your-github-id"
GITHUB_CLIENT_SECRET="your-github-secret"

# Pusher
PUSHER_APP_ID="your-pusher-app-id"
PUSHER_KEY="your-pusher-key"
PUSHER_SECRET="your-pusher-secret"
PUSHER_CLUSTER="your-pusher-cluster"
NEXT_PUBLIC_PUSHER_KEY="your-pusher-key"
NEXT_PUBLIC_PUSHER_CLUSTER="your-pusher-cluster"

# Cloudinary (for image uploads)
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME="your-cloudinary-name"
NEXT_PUBLIC_CLOUDINARY_UPLOAD_PRESET="your-cloudinary-preset"
CLOUDINARY_API_KEY="your-cloudinary-api-key"
CLOUDINARY_API_SECRET="your-cloudinary-api-secret"
```

4. **Database Setup**
```bash
# Generate Prisma client
npx prisma generate

# Push database schema
npx prisma db push
```

5. **Run the development server**
```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## 📁 Project Structure

```
src/
├── actions/
├── app/
│   ├── (auth)/
│   ├── api/
│   │   ├── auth/
│   │   ├── call/
│   │   ├── chat/
│   │   ├── contact/
│   │   ├── cron/markInactiveUsersOffline
│   │   ├── message/
│   │   ├── pusher/
│   │   ├── users/
│   ├── calls/
│   ├── chat/
│   ├── contact/
│   ├── global.css
│   └── layout.tsx
├── components/
│   ├── auth/
│   ├── chat-ui/
│   ├── dialogs/
│   ├── loading-states/
│   ├── others/
│   ├── sidebar/
│   ├── ui/
│   └── user-profile/
├── contexts/
├── hooks/
├── libs/
└── types/
```

## 🎨 UI/UX Features

- **Modern Design**: Clean, intuitive interface with Tailwind CSS
- **Dark/Light Mode**: Theme switching support
- **Responsive Layout**: Mobile-first design approach
- **Loading States**: Smooth loading animations and skeletons
- **Error Handling**: User-friendly error messages and retry mechanisms
- **Accessibility**: ARIA labels and keyboard navigation support

## 🔒 Security Features

- **JWT Authentication**: Secure session management
- **Rate Limiting**: Protection against spam and abuse
- **Input Validation**: Server-side validation for all inputs
- **CORS Protection**: Proper cross-origin resource sharing setup
- **Environment Variables**: Secure configuration management

## 📝 API Documentation

### Authentication Endpoints
- `POST /api/auth/signin` - User login
- `POST /api/auth/signup` - User registration
- `POST /api/auth/signout` - User logout

### Messaging Endpoints
- `GET /api/conversations` - Get user conversations
- `POST /api/conversations` - Create new conversation
- `GET /api/conversations/[id]/messages` - Get conversation messages
- `POST /api/messages` - Send new message

### User Management
- `GET /api/users` - Get all users
- `GET /api/users/[id]` - Get user profile
- `PUT /api/users/[id]` - Update user profile

## 👨‍💻 Author

**Aditya Tekale**
- GitHub: [@adityatekale27](https://github.com/adityatekale27)
- LinkedIn: [linkedin.com/in/adityatekale](https://linkedin.com/in/adityatekale)
- Email: aditekale27@gmail.com

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React framework
- [Pusher](https://pusher.com/) - Real-time messaging infrastructure
- [Prisma](https://prisma.io/) - Database toolkit
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [NextAuth.js](https://next-auth.js.org/) - Authentication solution

---

⭐ If you found this project helpful, please give it a star on GitHub!
