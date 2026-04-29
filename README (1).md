# 🏢 Smart Visitor & Vehicle Management System

> Full-stack cloud + AI system for real-time visitor tracking and automated vehicle number plate recognition using Node.js, Python ML service, and MongoDB.

![Node.js](https://img.shields.io/badge/Node.js-20-green) ![Python](https://img.shields.io/badge/Python-3.11-blue) ![MongoDB](https://img.shields.io/badge/MongoDB-7-green) ![Docker](https://img.shields.io/badge/Docker-ready-blue)

## ✨ Features
- 🔐 JWT authentication with Role-Based Access Control (RBAC)
- 🚗 AI-powered vehicle number plate detection (OCR + OpenCV)
- 📡 Real-time updates via Socket.IO
- 🏗️ Microservices architecture (Node.js backend + Python ML service)
- 🍃 MongoDB database with event-driven design
- 🐳 Docker Compose orchestration

## 🏗️ Architecture
```
Client
  │
  ├── REST API (Node.js/Express :3000)
  │     ├── JWT Auth & RBAC
  │     ├── Visitor Management
  │     └── Vehicle Management
  │
  └── ML Service (Python/FastAPI :8001)
        └── Vehicle Plate Detection (OpenCV + Tesseract)

MongoDB ←── Both services
```

## 🚀 Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/smart-visitor-vehicle-system.git
cd smart-visitor-vehicle-system
cp .env.example .env
docker-compose up --build
```

Backend runs at `http://localhost:3000`  
ML service runs at `http://localhost:8001`

## 📡 API Endpoints

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| POST | /api/auth/login | No | Get JWT token |
| GET | /api/visitors | Yes | List visitors |
| POST | /api/vehicles/detect | Yes | Detect vehicle plate |
| GET | /health | No | Health check |

## 📁 Project Structure
```
smart-visitor-vehicle-system/
├── backend/
│   └── src/
│       ├── server.js           # Express + Socket.IO
│       ├── middleware/auth.js  # JWT + RBAC
│       └── routes/
├── ml_service/
│   └── vehicle_detector.py    # OCR plate detection
├── docker-compose.yml
└── .env.example
```

## 🧪 Tests
```bash
cd backend && npm test
cd ml_service && pytest tests/
```

## 👨‍💻 Author
**Mallikarjuna Purni** — Cloud & AI MLOps Engineer
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/mallikarjuna-purni-a8185628b/)
