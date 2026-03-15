# Task Optimizer

Task Optimizer is a **full-stack AI system** that detects employee mood and emotion, recommends suitable tasks, tracks mood history, and provides team analytics with stress alerts.

---

## Tech Stack

### Frontend

* React
* TypeScript
* Vite
* Recharts

### Backend

* Flask
* SQLAlchemy

### AI

* Text sentiment analysis using **TextBlob**
* Webcam emotion detection using **OpenCV**

### Database

* SQLite (default)
* PostgreSQL (optional)

---

## Features

* Real-time emotion detection (text + webcam)
* Task recommendation based on emotion
* Historical mood tracking per employee
* Stress alerts for consecutive stressed streaks
* Team mood analytics dashboard
* Privacy-aware design (employee IDs only)

---

## Project Structure

backend/ → Flask API service and AI logic
frontend/ → React dashboard
docker-compose.yml → Optional PostgreSQL setup

---

## Backend Setup

### Configure environment

Copy:

backend/.env.example → backend/.env

### Create virtual environment

cd backend
python -m venv .venv
.venv\Scripts\activate

### Install dependencies

pip install -r requirements.txt

### Run API

python -m app.main

### Optional PostgreSQL

Run:

docker compose up -d

Set DATABASE_URL in backend/.env

API Base URL:

http://localhost:8000/api/v1

---

## Frontend Setup

### Configure environment

Copy:

frontend/.env.example → frontend/.env

### Install and run

cd frontend
npm install
npm run dev

App URL:

http://localhost:5173

---

## Main API Endpoints

POST /api/v1/emotion/detect
POST /api/v1/emotion/detect/webcam
GET /api/v1/employees/{employee_id}/mood-history
GET /api/v1/teams/{team_id}/analytics
GET /api/v1/alerts
GET /api/v1/health

---

## Privacy Notes

* Use anonymized employee_id and team_id identifiers.
* Do not send personal identifiers in payloads.
* Store only required operational data.

---

## Author

Naraboina Manoj Kumar
