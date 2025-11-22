
# 👁️ Eye Contact Coach

An AI-powered web application that helps users improve their eye contact skills using real-time webcam tracking and facial recognition technology.

![Eye Contact Coach](https://img.shields.io/badge/Next.js-14-black?style=flat&logo=next.js)
![React](https://img.shields.io/badge/React-18-blue?style=flat&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat&logo=typescript)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3-38bdf8?style=flat&logo=tailwind-css)

## 🌟 Features

### Core Features
- **Real-time Eye Contact Detection** - AI-powered facial recognition using face-api.js and TensorFlow.js
- **Live Feedback** - Instant visual indicators showing when you're maintaining good eye contact
- **Session Tracking** - Record and analyze your practice sessions over time
- **Analytics Dashboard** - Comprehensive statistics and progress tracking
- **Session History** - View past sessions with detailed metrics and charts
- **Export & Share** - Export session data as CSV or generate shareable links

### Pro Mode Features ✨
- **Virtual Audience** - Practice with realistic human avatars simulating real audiences
- **Multiple Scenarios**:
  - Job Interviews (3 people)
  - Presentations (5 people)
  - Team Meetings (4-5 people)
  - Panel Discussions (6+ people)
- **Engagement Balance Tracking** - Measures how evenly you engage all audience members
- **Gaze Distribution Analytics** - Visual breakdown of attention across each person
- **Audience Reactions** - Dynamic feedback from virtual audience members
- **Customizable Settings** - Adjust audience size, layout, and reaction sensitivity

### User Experience
- **Secure Authentication** - Email/password and Google SSO support
- **Responsive Design** - Works seamlessly on desktop and mobile devices
- **Dark/Light Mode** - Theme support for comfortable practice sessions
- **Settings Customization** - Personalize goals, thresholds, and preferences
- **Progress Tracking** - Monitor improvement over weeks and months

## 🚀 Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **React 18** - UI library
- **TypeScript 5** - Type safety
- **TailwindCSS 3** - Utility-first styling
- **Shadcn/ui** - Beautiful component library
- **Framer Motion** - Smooth animations

### AI/ML
- **face-api.js** - Face detection and landmark recognition
- **TensorFlow.js** - Machine learning in the browser
- **Real-time tracking** - 30fps gaze direction analysis

### Backend
- **Next.js API Routes** - Serverless backend
- **PostgreSQL** - Database
- **Prisma** - ORM for database access
- **NextAuth.js** - Authentication

### Deployment
- **Vercel/Abacus.AI** - Hosting platform
- **Cloud Storage** - Avatar assets

## 📋 Prerequisites

- Node.js 18+ and yarn
- PostgreSQL database
- Modern web browser with webcam access

## 🛠️ Installation

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/eye-contact-coach.git
cd eye-contact-coach/nextjs_space
```

2. **Install dependencies**
```bash
yarn install
```

3. **Set up environment variables**

Create a `.env` file in the root directory:

```env
# Database
DATABASE_URL="postgresql://user:password@localhost:5432/eye_contact_coach"

# NextAuth
NEXTAUTH_SECRET="your-secret-key-here"
NEXTAUTH_URL="http://localhost:3000"

# Google OAuth (optional)
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
```

4. **Set up the database**
```bash
yarn prisma generate
yarn prisma db push
```

5. **Run the development server**
```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📱 Usage

### Getting Started

1. **Sign up** for an account or log in
2. **Allow webcam access** when prompted
3. **Start a session** from the dashboard
4. **Practice** maintaining eye contact with the camera
5. **Review** your performance in the analytics section

### Pro Mode

1. Enable **Pro Mode** toggle on the dashboard
2. Select your **scenario** (Interview, Presentation, etc.)
3. Choose **audience size** (3-10 people)
4. Start practicing with the **virtual audience**
5. Monitor your **engagement balance** in real-time
6. View **gaze distribution** across all audience members

### Tips for Best Results

- Ensure good lighting conditions
- Position your camera at eye level
- Maintain a comfortable distance (2-3 feet)
- Practice in short sessions (5-10 minutes)
- Track your progress over time

## 📊 How It Works

### Eye Contact Detection

1. **Face Detection** - Identifies your face in the webcam feed using TinyFaceDetector
2. **Landmark Detection** - Locates 68 facial landmarks including eyes
3. **Gaze Estimation** - Calculates eye position and direction
4. **Contact Determination** - Determines if you're looking at the camera (or specific audience zones in Pro Mode)
5. **Metrics Tracking** - Records duration, streaks, and distribution

### Engagement Balance Algorithm

```
balance = 100 - (standardDeviation / average) × 100
```

Where:
- **standardDeviation** = spread of gaze time across audience members
- **average** = mean gaze time per person
- **Higher balance** (80%+) = even engagement across all members
- **Lower balance** (<60%) = focused on specific individuals

## 🎯 Key Metrics

- **Eye Contact %** - Percentage of session spent maintaining eye contact
- **Duration** - Total practice time
- **Current Streak** - Longest continuous eye contact period
- **Max Streak** - Best streak achieved
- **Engagement Balance** - (Pro Mode) How evenly you engage the audience
- **Gaze Distribution** - (Pro Mode) Time spent looking at each person

## 🔒 Privacy & Security

- **Local Processing** - All AI/ML runs in your browser
- **No Video Storage** - Webcam feed is not recorded or transmitted
- **Secure Authentication** - Passwords hashed with bcrypt
- **HTTPS Only** - All data transmitted securely
- **Session Data** - Only metrics stored, no video/images

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **face-api.js** - Amazing face detection library
- **TensorFlow.js** - Machine learning in JavaScript
- **Shadcn/ui** - Beautiful component library
- **Vercel** - Hosting and deployment
- **Abacus.AI** - Development platform

## 📧 Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter)

Project Link: [https://github.com/YOUR_USERNAME/eye-contact-coach](https://github.com/YOUR_USERNAME/eye-contact-coach)

## 🌐 Live Demo

Check out the live app: [https://eye-contact-coach-9ebyjx.abacusai.app](https://eye-contact-coach-9ebyjx.abacusai.app)

**Test Credentials:**
- Email: test@example.com
- Password: password123

---

Made with ❤️ using Next.js, React, and AI
