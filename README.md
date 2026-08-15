# 🎮 Game Over: Premium Gaming Lounge

A state-of-the-art, glassmorphic web application built for a premium gaming lounge. It features a high-performance scroll-synced background animation, dynamic game library filtering, and a robust universal booking system.

![Game Over Preview](https://images.unsplash.com/photo-1550745165-9bc0b252726f?q=80&w=1200&auto=format&fit=crop)

## ✨ Features

- **Scroll-Synced Cinematic Hero:** Uses a fixed `<canvas>` element mapping 240 frames of animation directly to the user's scroll position for a breathtaking entrance.
- **Dynamic Game Library:** Real-time filtering by platform (PS5, PC, etc.) with stunning hover effects, neon accents, and responsive grid layouts.
- **Universal Booking System:** A modular, reusable booking flow for every activity (Car Simulators, PlayStation, VR, Massage Chairs).
  - Automatically generates dynamic time slots based on session duration.
  - Mock QR code payment gateway.
  - Automated Queue Number generation (e.g., `Q-104`).
- **Glassmorphic UI:** Utilizes Tailwind CSS to create a premium frosted-glass aesthetic with deep zinc backgrounds, teal typography, and pink ambient glows.

## 🏗️ Architecture

The project is strictly separated into a clean architecture for easy deployment:

### `frontend/`
A pure frontend application (`index.html` + assets) built with HTML, Tailwind CSS, and Vanilla JavaScript. It fetches data dynamically from the backend API.

### `backend/`
A lightweight, zero-dependency Node.js API built using native HTTP modules (`server.js` + `data.json`). No heavy `node_modules` required.

## 🚀 Deployment

### 1. Deploy the Backend
The backend can be easily deployed to a service like **Render** or **Railway**:
- Connect the repository and point the Root Directory to `backend`.
- Set the start command to `npm start`.

### 2. Deploy the Frontend
Once the backend is live, update the fetch URL in `frontend/index.html`:
```javascript
const response = await fetch('YOUR_LIVE_BACKEND_URL/api/games');
```
Then, host the `frontend` folder using **GitHub Pages**, **Vercel**, or **Netlify**.

## 🛠️ Local Development

To run the project locally, you will need to start both the frontend and backend servers.

**Start the Backend (Port 3000):**
```bash
cd backend
node server.js
```

**Start the Frontend (Port 8080):**
```bash
cd frontend
python -m http.server 8080
```

Open `http://localhost:8080` in your browser.

---
*Built with ❤️ for gamers.*
