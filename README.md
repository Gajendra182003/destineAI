# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# ✈️ DestinAI — An AI-Powered Personalized Travel Planning System

<div align="center">

![DestinAI Banner](https://img.shields.io/badge/DestinAI-Travel%20Planning-blue?style=for-the-badge&logo=airplane&logoColor=white)
![React](https://img.shields.io/badge/React.js-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Azure](https://img.shields.io/badge/Azure_AI-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)

> **Major Project 1 Synopsis** — Saraswati College of Engineering, Kharghar, Navi Mumbai  
> Department of Computer Science & Engineering (Data Science) | Academic Year 2024–25

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [System Flow](#-system-flow)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Team](#-team)
- [Acknowledgements](#-acknowledgements)

---

## 🌍 Overview

**DestinAI** is a cutting-edge web platform designed to revolutionize trip planning and enhance the overall travel experience. It serves as a **dual-purpose platform** connecting tourists with curated travel itineraries and empowering travel agencies to reach budget-conscious travelers.

- **For Tourists** — Personalized itinerary recommendations, real-time maps, hotel suggestions, enquiry system, and downloadable PDFs.
- **For Travel Agencies** — An intuitive dashboard to upload & manage packages with dynamic pricing, seasonal discounts, and real-time booking notifications.

Built on the **PERN stack** (PostgreSQL, Express.js, React.js, Node.js) and integrated with **Azure AI APIs**, **Google Maps API**, and **Stripe**, DestinAI makes travel planning seamless, intelligent, and affordable.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 **AI-Powered Itineraries** | Machine learning generates personalized travel plans based on budget, days, and group size |
| 🗺️ **Real-Time Maps** | Google Maps API integration for location-based activity suggestions |
| 💬 **Trip Assistant Chatbot** | Instant support and recommendations via AI chatbot |
| 💱 **Currency Converter** | Real-time currency conversion for accurate cost planning |
| 📄 **PDF Itinerary Export** | Download detailed day-by-day itineraries as PDF |
| 🏨 **Hotel Recommendations** | AI-curated hotel suggestions per destination and budget |
| 🔐 **Google Authentication** | Secure sign-in with role selection (Traveler / Agency) |
| 📊 **Agency Dashboard** | Enquiry statistics, package management, and dynamic pricing |
| 🌱 **Sustainability Focus** | Eco-friendly travel options and sustainability ratings |
| ⭐ **Community Reviews** | Traveler-generated ratings, reviews, and a personalized news feed |

---

## 🏗️ System Architecture

```mermaid
graph TB
    subgraph Client["🖥️ Client Layer (React.js + Tailwind CSS)"]
        UI[User Interface]
        TravelerDash[Traveler Dashboard]
        AgencyDash[Agency Dashboard]
        Chatbot[AI Chatbot Widget]
        CurrencyConv[Currency Converter]
    end

    subgraph Auth["🔐 Authentication"]
        GoogleAuth[Google OAuth 2.0 / Firebase]
    end

    subgraph Backend["⚙️ Backend Layer (Node.js + Express.js)"]
        API[REST API Server]
        ML[ML Recommendation Engine]
        NLP[NLP Interface]
        RealTime[Real-Time Event Handler]
    end

    subgraph AI["🤖 AI & External APIs"]
        AzureAI[Azure AI APIs]
        GoogleMaps[Google Maps API]
        Stripe[Stripe Payment API]
        ChartJS[Chart.js Analytics]
    end

    subgraph DB["🗄️ Database Layer"]
        PostgreSQL[(PostgreSQL)]
        Firebase2[(Firebase)]
    end

    UI --> GoogleAuth
    GoogleAuth --> TravelerDash
    GoogleAuth --> AgencyDash
    TravelerDash --> API
    AgencyDash --> API
    Chatbot --> AzureAI
    CurrencyConv --> API

    API --> ML
    API --> NLP
    API --> RealTime
    ML --> AzureAI
    NLP --> AzureAI
    API --> GoogleMaps
    API --> Stripe
    AgencyDash --> ChartJS

    API --> PostgreSQL
    API --> Firebase2
```

---

## 🛠️ Tech Stack

### Frontend
- **React.js** — Component-based UI framework
- **Tailwind CSS** — Utility-first styling
- **Chart.js** — Data visualization for Agency Dashboard
- **Vite** — Fast development build tool

### Backend
- **Node.js** — JavaScript runtime
- **Express.js** — RESTful API server

### Database
- **PostgreSQL** — Relational database for structured data
- **Firebase** — Real-time backend for auth and live data

### AI & Integrations
- **Azure AI APIs** — Intelligent trip planning and NLP chatbot
- **Google Maps API** — Location services and real-time mapping
- **Stripe API** — Secure payment processing
- **Google OAuth 2.0** — Authentication

---

## 🔄 System Flow

```mermaid
flowchart TD
    A([🏠 DestinAI Homepage]) --> B[User Login / Sign Up]
    B --> C{Select Role}

    C -->|Traveler| D[🧳 Traveler Dashboard]
    C -->|Agency| E[🏢 Agency Dashboard]

    D --> F[Browse Itineraries]
    F --> G[Personalized Recommendations\nML-based filtering]
    G --> H[View Trip Details\nHotel, Map, Activities]
    H --> I{User Action}
    I --> J[📧 Make Enquiry]
    I --> K[📄 Download PDF Itinerary]
    I --> L[💳 Secure Payment via Stripe]

    E --> M[Upload & Manage Itineraries]
    M --> N[Add Trip Details\n+ Dynamic Pricing]
    N --> O[📊 View Enquiry Statistics]
    O --> P[Respond to Enquiries\nChat / Call]

    style A fill:#4F46E5,color:#fff
    style D fill:#059669,color:#fff
    style E fill:#D97706,color:#fff
    style G fill:#7C3AED,color:#fff
```

---

## 📸 Screenshots

> 📁 **Tip:** Place your screenshot images in a `/screenshots` folder at the root of your repo and update the paths below.

### 🏠 Homepage
![Homepage](./screenshots/homepage.png)
> User-friendly landing page with AI-powered personalization highlights and quick access to the chatbot and currency converter.

---

### 🔐 Sign In & Role Selection
![Sign In](./screenshots/sign-in.png)
> Secure Google Authentication with role selection — choose between **Traveler** or **Agency** for a customized experience.

---

### 🗺️ Choose Your Destination
![Choose Destination](./screenshots/choose-destination.png)
> Dynamic trip exploration interface — filter packages by location, budget, duration, and group size.

---

### 📦 Package Details & Hotel Recommendations
![Package Selected](./screenshots/package-selected.png)
> Detailed view of a selected trip package with destination info, travel duration, budget tier, and AI-curated hotel recommendations.

---

### 📊 Agency Dashboard
![Agency Dashboard](./screenshots/agency-dashboard.png)
> Intuitive agency control panel showing enquiry statistics per trip, with options to manage packages and respond to bookings.

---

### 📄 Download Itinerary as PDF
![Download PDF](./screenshots/download-pdf.png)
> Day-by-day sightseeing recommendations with estimated visit durations and a one-click PDF download option.

---

### 💱 Currency Converter
![Currency Converter](./screenshots/currency-converter.png)
> Real-time currency converter overlay for accurate cost estimation during trip planning.

---

### 💬 AI Chatbot
![Chatbot](./screenshots/chatbot.png)
> Instant assistance chatbot for quick support and travel recommendations.

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+
- PostgreSQL
- Firebase project configured
- API keys: Azure AI, Google Maps, Stripe

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/destinai.git
cd destinai

# 2. Install dependencies for backend
cd server
npm install

# 3. Install dependencies for frontend
cd ../client
npm install
```

### Environment Variables

Create a `.env` file in the `/server` directory:

```env
# Database
DATABASE_URL=postgresql://user:password@localhost:5432/destinai

# Firebase
FIREBASE_API_KEY=your_firebase_api_key
FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com

# Azure AI
AZURE_AI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_AI_KEY=your_azure_api_key

# Google APIs
GOOGLE_MAPS_API_KEY=your_google_maps_key

# Stripe
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_PUBLIC_KEY=your_stripe_public_key
```

### Running the App

```bash
# Start backend server
cd server
npm run dev

# Start frontend (in a new terminal)
cd client
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 📁 Project Structure

```
destinai/
├── client/                  # React.js Frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   │   ├── Chatbot/
│   │   │   ├── CurrencyConverter/
│   │   │   └── Map/
│   │   ├── pages/           # Route-level pages
│   │   │   ├── HomePage/
│   │   │   ├── TravelerDashboard/
│   │   │   └── AgencyDashboard/
│   │   ├── hooks/           # Custom React hooks
│   │   └── utils/           # Helper functions
│   └── public/
│
├── server/                  # Node.js + Express Backend
│   ├── routes/              # API route handlers
│   ├── controllers/         # Business logic
│   ├── models/              # Database models
│   ├── middleware/          # Auth & validation middleware
│   └── services/            # External API integrations
│       ├── azureAI.js
│       ├── googleMaps.js
│       └── stripe.js
│
├── screenshots/             # App screenshots for README
├── .env.example
└── README.md
```

---

## 👥 Team

| Roll No | Name |
|---|---|
| 43 | Prathamesh Nipane |
| 56 | Gajendra Rathod |
| 60 | Sohel Sayyed |
| 68 | Omkar Suwar |

> **Guide:** Prof. Ragini Sharma  
> **Project Coordinator:** Prof. Sarita Kale  
> **Head of Department:** Prof. Ragini Sharma  
> **Principal:** Dr. Manjusha Deshmukh

---

##  Acknowledgements

We express our sincere gratitude to:

- **Prof. Ragini Sharma** — Project Guide & HOD, for constant inspiration and guidance
- **Prof. Sarita Kale** — Project Coordinator, for kind support throughout the project
- **Dr. Manjusha Deshmukh** — Principal, Saraswati College of Engineering
- All staff of the **Department of Computer Science & Engineering (Data Science)**

> *Saraswati College of Engineering, Kharghar, Navi Mumbai — NAAC A+ Accredited*  
> *(Affiliated to University of Mumbai)*

---

## 📄 License

This project was developed as part of the academic curriculum at Saraswati College of Engineering, Navi Mumbai (2024–25). All rights reserved by the respective authors.

---

<div align="center">
  <sub>Built with ❤️ by Team DestinAI · Saraswati College of Engineering · 2024–25</sub>
</div>
