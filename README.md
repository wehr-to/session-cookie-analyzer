# 🕸️ Session Hijack & Cookie Analyzer (FastAPI)

## 🎯 Purpose
A full-stack playground for demonstrating and testing session hijacking techniques and cookie misconfigurations:
- Simulate missing `HttpOnly`, `Secure`, `SameSite` flags
- Inject JavaScript in sandbox to capture cookies
- Replay session cookies using Python script
- Evaluate session expiration, regeneration, and fixation flaws

## 🔧 Tech Stack
- **Backend**: FastAPI
- **Frontend**: HTML + JS sandbox
- **Client**: Python script to simulate cookie replay attacks

## 🔐 Security Value
- **OWASP A01**: Broken Access Control
- **OWASP A07**: Identification and Authentication Failures
- Explains:
  - How session tokens behave under poor configurations
  - How to mitigate hijack, fixation, and replay
  - What to watch for during audits and interviews

## 🔨 Features
- Toggle secure/insecure cookie behaviors (`HttpOnly`, `Secure`, `SameSite`)
- Run JavaScript to simulate real-world cookie theft
- Python client that replays stolen cookies
- Visualize cookie contents and behavior in browser
- Dockerized for easy lab setup

## 🚀 Getting Started
```bash
# Clone the repo
$ git clone https://github.com/yourusername/session-cookie-analyzer.git
$ cd session-cookie-analyzer

# Run locally
$ python3 -m venv venv && source venv/bin/activate
$ pip install -r requirements.txt
$ python run.py

# Or use Docker
$ docker-compose up --build
```

## ✅ To Do
- [ ] Add session fixation toggle
- [ ] Show session regeneration logic on login
- [ ] Support multi-user sessions for realism
- [ ] Auto-rotate vulnerable settings every 5 mins (demo mode)

## 📄 License
MIT
