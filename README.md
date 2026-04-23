# 🍔 BhaiTuKha — Online Food Ordering Platform

BhaiTuKha is a full-stack React + Firebase food delivery web app that lets users browse restaurants, order dishes, track deliveries, and chat with an AI-powered food assistant. It is designed for speed, scalability, and modern UI.

---

## 🚀 Features

### 🏠 User Experience
- Restaurant Discovery: Browse 12 themed restaurants (Indian, Italian, Vegan, Chinese, etc.)
- Search & Filters: Search dishes and filter by cuisine type
- Interactive UI: Smooth animations and responsive design using Tailwind CSS
- Dynamic Offers: “Daily Deals” with clickable promo cards

### 🛒 Ordering & Tracking
- Add/remove dishes to cart
- Place and track live orders (with mock analytics)
- Auto-detect delivery address using Geolocation + OpenStreetMap
- “Track” and “History” views for active and completed orders

### 🔐 Authentication
- Firebase Authentication (Email/Password, Google Sign-In)
- Persistent user session and profile page
- Sign out and re-login supported

### 🤖 Chatbot (Gemini API)
- Built-in Gemini 2.5 Flash Preview API for AI food recommendations
- Smart conversational interface themed to match BhaiTuKha
- Typing animation, message history, and error handling

### 📊 Analytics
- Custom in-app analytics logger (page views, clicks, orders)
- Console-based analytics tracking

### 🌙 Visuals
- Polished React components with Tailwind CSS
- 3D animated food ring using THREE.js
- Fully responsive layout for desktop and mobile

---

## 🧠 Tech Stack

| Layer | Technology |
|-------|-------------|
| Frontend | React (Vite) + Tailwind CSS |
| Backend | Firebase Firestore + Firebase Auth |
| AI Assistant | Gemini API (Google Generative Language) |
| Deployment | Vercel |
| Other | THREE.js (3D visuals), Lucide Icons, Geolocation API |

---

## 🧩 Folder Structure (Simplified)

```text
BhaiTuKha/
├── src/
│   ├── App.jsx
│   ├── firebase.js
│   ├── assets/
│   ├── index.css
│   └── main.jsx
├── package.json
├── vite.config.js
└── README.md 
```
---

## ⚙️ Installation

### 1️⃣ Clone the repository
```text
git clone https://github.com/Yatishydv/BhaiTuKha.git
cd BhaiTuKha
```
### 2️⃣ Install dependencies
```text
npm install
```
### 3️⃣ Configure Firebase
Create a file named `firebase.js` inside the `src` folder:
```text
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";

const firebaseConfig = {
apiKey: "YOUR_FIREBASE_API_KEY",
authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
projectId: "YOUR_PROJECT_ID",
storageBucket: "YOUR_PROJECT_ID.appspot.com",
messagingSenderId: "YOUR_SENDER_ID",
appId: "YOUR_APP_ID",
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const db = getFirestore(app);
export default app;
```
### 4️⃣ Run the development server
```text
npm run dev
Open http://localhost:5173 in your browser.
```
---

## 🌐 Deployment on Vercel

1. Push your repo to GitHub
2. Go to https://vercel.com
3. Import your project → choose “React (Vite)”
4. Add environment variables (Firebase and Gemini API keys)
5. Deploy 🚀

---

## 🧪 Environment Variables

| Key | Description |
|-----|--------------|
| VITE_FIREBASE_API_KEY | Firebase API key |
| VITE_GEMINI_API_KEY | Gemini API key |
| VITE_FIREBASE_PROJECT_ID | Firebase project ID |
| VITE_FIREBASE_AUTH_DOMAIN | Firebase auth domain |

---

## 💬 Chatbot API Usage

The chatbot uses the Gemini 2.5 Flash Preview API:

POST https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=YOUR_API_KEY
This provides fast, context-aware food suggestions and answers.

---

## 🧑‍💻 Developer

👨‍🎨 Designed & Developed by [Yatish 🌸](https://www.instagram.com/yatishydv/)  
© 2025 Foodzy. All rights reserved.

---

## 🧱 Future Enhancements
- Real-time order tracking with Firestore
- Payment gateway integration (Razorpay/Stripe)
- Admin dashboard for restaurants
- Push notifications for order updates
- Advanced dark mode with animations
