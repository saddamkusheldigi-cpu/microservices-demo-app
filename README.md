# 🍏 Multi-Container Fruit Service (Docker Compose Stack)

A lightweight microservices-based web application built using **Docker Compose**. This project connects a **Python Flask REST API** backend with a **PHP Apache** frontend inside isolated containers.

---

## 🏗️ Project Architecture


             [ User Browser ]
                    │
                    ▼  (Port 5000)
         ┌─────────────────────┐
         │   PHP Web Server    │
         │     (website)       │
         └──────────┬──────────┘
                    │
                    │  Internal Docker Network
                    │  (http://fruit-service)
                    ▼
         ┌─────────────────────┐
         │  Python REST API    │
         │   (fruit-service)   │
         └─────────────────────┘

         ---

## 🛠️ Tech Stack & Services

- **Frontend:** PHP 8, Apache Web Server
- **Backend API:** Python 3, Flask, Flask-RESTful
- **Containerization & Orchestration:** Docker, Docker Compose

---

## 📁 Repository Structure

```text
.
├── product/
│   ├── api.py              # Python Flask API logic
│   ├── requirements.txt    # Python dependencies (flask, flask-restful)
│   └── Dockerfile          # Docker setup for Python API
├── website/
│   └── index.php           # PHP Webpage requesting data from Python API
└── docker-compose.yaml     # Orchestrates both services


🚀 Getting Started
Prerequisites
Make sure you have installed:

Docker

Docker Compose

Installation & Run
Clone the repository:

Bash
git clone [https://github.com/saddamkusheldigi-cpu/microservices-demo.git]
(https://github.com/saddamkusheldigi-cpu/microservices-demo.git]


Start the application stack:

Bash
docker compose up -d



Access the application:

PHP Frontend: Open http://localhost:5000 (or http://<YOUR_SERVER_IP>:5000)

Python API Endpoint: Open http://localhost:5001 (or http://<YOUR_SERVER_IP>:5001)

⚙️ Useful Commands
Check running containers:

Bash
docker compose ps
View service logs:

Bash
docker compose logs -f
Rebuild containers after code changes:

Bash
docker compose up -d --build
Stop and remove containers:

Bash
docker compose down

---
