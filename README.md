# Multi-User MCP Server with Chatbot and Agent

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green?logo=fastapi)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-brightgreen?logo=mongodb)
![Heroku](https://img.shields.io/badge/Heroku-Ready-purple?logo=heroku)

---

## 🚀 Overview
A full-stack web application implementing the Model Context Protocol (MCP) to provide two AI assistant experiences:
- **Chatbot**: Conversational Q&A
- **Agent**: Tool-using AI agent

Features include user authentication, persistent chat history, real-time WebSocket messaging, and file upload for document analysis. The app is production-ready and deployable on Heroku.

---

## ✨ Features
- **User Authentication**: Registration, login, password recovery, email verification
- **Dual AI Interfaces**: Chatbot and Agent, each with unique capabilities
- **Real-Time Chat**: WebSocket-based instant messaging
- **Conversation History**: Persistent, user-specific chat logs
- **File Upload**: Analyze documents in chat
- **MCP Server Integration**: Connects to multiple MCP servers for tool execution
- **Responsive UI**: Clean, mobile-friendly HTML/CSS/JS frontend
- **Heroku Deployment**: Ready for cloud deployment

---

## 🛠️ Tech Stack
- **Backend**: Python 3.10+, FastAPI, MongoDB, Uvicorn
- **Frontend**: HTML, CSS, Vanilla JavaScript (see `static/`)
- **AI Integration**: OpenAI API or compatible LLM providers
- **Real-Time**: WebSocket
- **Deployment**: Heroku (Procfile included)

---

## 📁 Project Structure
```
.
├── main.py                # FastAPI app entry point
├── routes/                # API route handlers (auth, chatbot, agent, feedback)
├── static/                # Frontend HTML, CSS, JS for all pages
│   ├── chatbot/           # Chatbot interface
│   ├── agent/             # Agent interface
│   ├── login/             # Login page
│   ├── register/          # Registration page
│   └── ...                # Other static assets
├── tools/                 # MCP server integration logic
├── email_config.py        # Email settings for verification
├── config.py              # General configuration
├── servers_config.json    # MCP server connection details
├── requirements.txt       # Python dependencies
├── Procfile               # Heroku process file
└── README.md              # This file
```

---

## ⚡ Getting Started

### Prerequisites
- Python 3.10+
- MongoDB (local or Atlas)
- Node.js (for MCP server dependencies)
- Heroku CLI (for deployment)

### Installation
1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd <repo-folder>
   ```
2. **Install Python dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
3. **Set up environment variables:**
   - Copy `.env.example` to `.env` and fill in your secrets (OpenAI key, MongoDB URI, email credentials).
4. **Install MCP server dependencies (if needed):**
   ```sh
   npm install
   ```
5. **Run the server locally:**
   ```sh
   python main.py
   ```
   The app will be available at `http://localhost:5000/`.

---

## 💡 Usage
- **Register**: `/register` to create a new account
- **Login**: `/login` to sign in
- **Chatbot**: `/chatbot` for general Q&A
- **Agent**: `/agent` for advanced tool-using AI
- **File Upload**: Use the file input in chat to upload documents
- **Conversation History**: View and revisit past conversations in the sidebar

---

## ☁️ Deployment
- **Heroku**: Ready for Heroku deployment. Use the included `Procfile` and set environment variables in the Heroku dashboard.
- **Static Files**: All frontend assets are served from the `static/` directory.

---

## 🔒 Security & Best Practices
- Authentication tokens stored securely (cookies/localStorage)
- Passwords hashed before storage
- Email verification required for new accounts
- CORS enabled for cross-origin requests

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License
This project is licensed under the MIT License.

---

## 🙏 Acknowledgements
- [FastAPI](https://fastapi.tiangolo.com/)
- [MongoDB](https://www.mongodb.com/)
- [OpenAI](https://openai.com/)
- [Heroku](https://heroku.com/)
