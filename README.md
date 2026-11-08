# 🌾 FarmTrust

> An intelligent, data-driven agricultural marketplace and price forecasting platform designed to bring price predictability, transparency, and seamless trade to farmers and buyers.

---

## 🚀 Overview

Agricultural supply chains often suffer from extreme price volatility, market opacity, and intermediaries that reduce profitability for farmers while inflating costs for buyers. **FarmTrust** provides a unified ecosystem that integrates fair price discovery, direct farmer-to-buyer trade, order management, and predictive time-series machine learning models to forecast crop prices.

---

## 🛠️ Tech Stack & Architecture

FarmTrust is architected with a decoupled microservice pattern:

* **Frontend:** [React.js](https://react.dev/), [Tailwind CSS](https://tailwindcss.com/), [Recharts](https://recharts.org/), [Framer Motion](https://www.framer.com/motion/), [Lucide React](https://lucide.dev/)
* **Core Backend:** [Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/), [Sequelize ORM](https://sequelize.org/) (MySQL / SQLite), [JWT](https://jwt.io/) & [Google OAuth 2.0](https://developers.google.com/identity)
* **AI Microservice:** [Python 3](https://www.python.org/), [FastAPI](https://fastapi.tiangolo.com/), [Prophet](https://facebook.github.io/prophet/) (Time-Series Forecasting), [Pandas](https://pandas.pydata.org/), [Uvicorn](https://www.uvicorn.org/)

---

## ✨ Key Features

- **🌾 Farmer Dashboard:** Manage crop listings, track inventory, view pending/confirmed orders, and monitor localized district pricing.
- **🛒 Buyer Marketplace:** Discover available crops directly from farmers, review quality specs, compare market prices, and place orders.
- **📈 AI Price Forecasting:** Powered by Facebook Prophet, providing time-series trend analysis and price projections across major crops to help farmers plan harvest timing and pricing.
- **🛡️ Admin & Moderation Portal:** Verify users, oversee crop listings, manage transactions, and inspect platform analytics.
- **🔐 Secure Authentication:** Role-based access control (Farmer, Buyer, Admin) with email/password verification and Google OAuth integration.

---

## 📁 Project Structure

```
FarmtrustDemo/
├── frontend/          # React Single Page Application (Tailwind CSS, Recharts)
├── backend/           # Node.js Express REST API & Sequelize Models
└── ai-service/        # FastAPI Python Microservice for Crop Price Forecasting
```

---

## ⚡ Getting Started

### Prerequisites
- **Node.js** (v18+ recommended)
- **Python** (v3.10 - 3.12 recommended)
- **MySQL** (or SQLite for local lightweight development)

---

### 1. AI Microservice Setup (FastAPI & Prophet)

```bash
cd ai-service

# Create and activate virtual environment
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install fastapi uvicorn pandas prophet

# Run the AI service (runs on http://127.0.0.1:8000)
uvicorn main:app --reload --port 8000
```

---

### 2. Backend Setup (Node.js & Express)

```bash
cd backend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with your database credentials, JWT secret, and email settings

# Start backend server (runs on http://localhost:5000)
npm run dev   # or npm start
```

---

### 3. Frontend Setup (React.js)

```bash
cd frontend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env

# Start React development server (runs on http://localhost:3000)
npm start
```

---

## 👥 The Team & Roles

* **Lead System Architect & AI Engineer** – System architecture, AI forecasting microservice, core backend API design & testing, landing page UI/UX
* **Security & Full-Stack Engineer** – Authentication flows, OAuth integration, and core user services
* **Frontend Engineer (Farmer Experience Lead)** – Farmer Dashboard & crop listing workflows
* **Frontend Engineer (Marketplace Lead)** – Buyer Dashboard & marketplace checkout experience
* **Operations & Backend Engineer** – Admin Portal, platform analytics, and governance

---

## 📄 License

This project was built for educational and demonstration purposes as a capstone project.
