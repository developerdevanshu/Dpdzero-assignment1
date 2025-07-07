# ✅ Dpdzero - DevOps Internship - Assignment 1 Completed

# 🚀 Multi-Service Docker Project with Nginx Reverse Proxy

This project sets up two backend services — one in **Go** and another in **Python (Flask)** — managed using **Docker Compose** and routed via an **Nginx reverse proxy**, allowing both to be accessed through a single port number.

---

## 📦 Services Overview

### 🐹 service_1 (Go)
A simple HTTP server written in Golang.

**Routes:**
- `GET /ping` → ✅ Health check
- `GET /hello` → 👋 Welcome message

### 🐍 service_2 (Python + Flask)
A basic Flask app providing similar endpoints.

**Routes:**
- `GET /ping` → ✅ Health check
- `GET /hello` → 👋 Welcome message

---

## 🌐 Nginx Reverse Proxy

Nginx runs in a Docker container and listens on port `8080`. It forwards incoming traffic to the correct service based on the URL path:

| 🔗 Path            | 🧭 Proxies To     | ⚙️ Description     |
|--------------------|------------------|--------------------|
| `/service1/*`      | 🐹 Go service    | Golang backend     |
| `/service2/*`      | 🐍 Flask service | Python backend     |

📄 Nginx also logs all requests with timestamps and paths to help with debugging and observability.

---

## 🛠️ How to Run the Project

> 🐳 Make sure **Docker** and **Docker Compose** are installed on your machine.

### ✅ Steps:

**🔹 Step 1:** 🚥 Clone the repository and navigate to the project directory:
```bash
git clone <https://github.com/developerdevanshu/Dpdzero-Devops-assignment1.git>
cd <Dpdzero-Devops-assignment1>
```

**🔹 Step 2:** 🏗️ Build and start all services using Docker Compose:
```bash
docker-compose up --build -d
```

**🔹 Step 3:** 🚦 Once all containers are running, Nginx will act as a reverse proxy and route requests to both services.<br>
You can now access the routes in your browser:

---

### 🌐 Go Service (service_1) 🐹

- 🔗 [http://localhost:8080/service1/ping](http://localhost:8080/service1/ping) &nbsp;—&nbsp; ✅ Health check
- 🔗 [http://localhost:8080/service1/hello](http://localhost:8080/service1/hello) &nbsp;—&nbsp; 👋 Welcome message

### 🌐 Python Flask Service (service_2) 🐍

- 🔗 [http://localhost:8080/service2/ping](http://localhost:8080/service2/ping) &nbsp;—&nbsp; ✅ Health check
- 🔗 [http://localhost:8080/service2/hello](http://localhost:8080/service2/hello) &nbsp;—&nbsp; 👋 Welcome message

---

✨ **Enjoy exploring your multi-service
