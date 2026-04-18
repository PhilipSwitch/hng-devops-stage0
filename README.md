# DevOps Stage 1 - Personal API

A simple Flask API deployed on a VPS using Nginx reverse proxy and systemd process management.

---

## 🌍 Live Deployment

**Base URL:**  
http://mobolaji-babajide.xyz

---

## 🚀 API Endpoints

### ✅ GET /

Response:
```json
{
  "message": "API is running"
}
```

### ✅ GET /health

Response:
```json
{
  "message": "healthy"
}
```

### ✅ GET /me

Response:
```json
{
  "name": "Mobolaji Philip Babajide",
  "email": "mobolaji0babajide@gmail.com",
  "github": "https://github.com/philipswitch"
}
```

All endpoints:
- Return `Content-Type: application/json`
- Return HTTP status `200`
- Respond in under 500ms

---

## 💻 Local Setup

Install dependencies:

```bash
pip3 install -r requirements.txt
```

Run the application:

```bash
python3 app.py
```

App runs locally on:

http://127.0.0.1:5000

---

## 🛠 Deployment Stack

- Python 3
- Flask
- Gunicorn
- Nginx (Reverse Proxy)
- Systemd (Process Manager)
- Ubuntu 22.04 LTS
- DigitalOcean VPS
- UFW Firewall (Ports 22, 80, 443 allowed)

---

## 🏗 Architecture

- Flask API runs internally on port 5000
- Gunicorn serves the application
- Nginx proxies public traffic (port 80) → 127.0.0.1:5000
- Systemd ensures the service runs persistently
- Firewall restricts unnecessary ports

---

## 📦 requirements.txt

```
Flask==3.0.0
gunicorn==21.2.0
```

---

## 🚫 .gitignore

```
__pycache__/
*.pyc
venv/
.env
```

---

## 🔄 Push to GitHub

```powershell
git init
git add .
git commit -m "DevOps Stage 1 - Personal API"

# After creating the repo on GitHub:
git remote add origin https://github.com/philipswitch/hng-devops.git
git branch -M main
git push -u origin main
```

---

## 👤 Author

Name: Mobolaji Philip Babajide  
Track: DevOps  
Stage: 1  
