# Chimera Protocol �

**CodeCraze Hackathon 2024 Submission**

A neural-themed AI memory management system that unifies multiple LLM providers into one collaborative platform with 3D brain visualization and persistent memory injection.

![Chimera Protocol](https://img.shields.io/badge/Chimera-Protocol-cyan)
![CodeCraze](https://img.shields.io/badge/CodeCraze-Hackathon-orange)
![License](https://img.shields.io/badge/license-MIT-green)
![Django](https://img.shields.io/badge/Django-5-green)
![React](https://img.shields.io/badge/React-18-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)
![Three.js](https://img.shields.io/badge/Three.js-3D-orange)

## Watch the [Demo Video](https://youtu.be/5OHoeqZk0Es)

## 🎯 The Problem We Solved

The AI industry is fragmented. OpenAI, Anthropic, Google, and others all operate in isolation: different APIs, different strengths, different ecosystems. Users are forced to choose one provider or juggle multiple accounts and interfaces. Worse, every time you switch models, you lose all context and have to start from scratch.

**Chimera Protocol unifies them all.**

## 💡 What Chimera Protocol Does

| The Problem | Our Solution |
|-------------|--------------|
| AI providers don't talk to each other | **Unified Multi-LLM Router**: One interface for all providers |
| Each model has different strengths | **Model Switching**: Use GPT-4 for code, Claude for writing, Gemini for analysis |
| AI has no persistent memory | **Memory Injection System**: Store knowledge and inject it into any model |
| Teams can't share AI context | **Collaborative Workspaces**: Teams share memories, conversations, and API keys |
| API keys scattered everywhere | **Encrypted Key Vault**: One secure place for all provider credentials |

## 🧬 The Chimera Architecture

```
        🧠 OpenAI (GPT-4o, GPT-4)
       /
      🧠 Anthropic (Claude 3.5 Sonnet)
     /
🦁--🧠 Google (Gemini 2.0 Flash)
     \
      🧠 Groq (Llama 3.3 70B) - FREE
       \
        🧠 DeepSeek (DeepSeek Chat)
```

Each "head" is a different AI provider, but they all share:
- **The same memory bank**: Inject context into any model
- **The same workspace**: Team members collaborate across providers
- **The same conversation history**: Switch models mid-conversation
- **The same secure storage**: One encrypted vault for all API keys

## ✨ Key Features

### Multi-LLM Support
| Provider | Models | Status |
|----------|--------|--------|
| OpenAI | GPT-4o, GPT-4, GPT-3.5-turbo | ✅ |
| Anthropic | Claude 3.5 Sonnet, Claude 3 | ✅ |
| Google | Gemini 2.0 Flash, Gemini Pro | ✅ |
| Groq | Llama 3.3 70B, Mixtral 8x7B | ✅ FREE |
| DeepSeek | DeepSeek Chat, DeepSeek Coder | ✅ |

### Memory System
- **Manual Creation**: Create memories with titles, content, and tags
- **URL Import**: Scrape and store content from web pages (Basic & Advanced modes)
- **File Import**: Import from PDF, DOCX, TXT, and more
- **Memory Injection**: Inject relevant context into any AI conversation
- **Semantic Search**: Find relevant memories by content

### 3D Brain Visualization
- Interactive Three.js brain model
- AI models displayed as glowing neural nodes
- Real-time connection visualization
- Cyberpunk-inspired interface

### Workspace & Team Collaboration
- Isolated workspaces per project
- Team collaboration with invites
- Role-based access control (Admin, Researcher, Observer)
- Real-time presence indicators

## 📦 Repository Structure

```
Chimera_Protocol/
├── Backend/     # Django REST API
└── Frontend/    # React/TypeScript UI
```

| Component | Tech Stack | Description |
|-----------|------------|-------------|
| **Backend** | Django 5, Python 3.11+, PostgreSQL | REST API, LLM routing, memory storage |
| **Frontend** | React 18, TypeScript 5, Three.js, Tailwind | 3D brain visualization, chat interface |

## 🚀 Quick Start

### Clone with Submodules

```bash
git clone --recurse-submodules https://github.com/ahammadshawki8/Chimera_Protocol.git
cd Chimera_Protocol
```

### Backend Setup

```bash
cd Backend
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
python generate_key.py
python manage.py migrate
python manage.py runserver
```

### Frontend Setup

```bash
cd Frontend
npm install
cp .env.example .env.local
npm run dev
```

## 🔧 Environment Variables

### Backend (.env)
```env
SECRET_KEY=your-django-secret-key
DEBUG=True
DATABASE_URL=postgres://user:pass@localhost:5432/chimera
ENCRYPTION_KEY=your-fernet-key
```

### Frontend (.env.local)
```env
VITE_API_BASE_URL=http://127.0.0.1:8000/api
```

## 🔌 API Highlights

| Endpoint | Description |
|----------|-------------|
| `POST /api/auth/register` | User registration |
| `POST /api/auth/login` | JWT authentication |
| `GET /api/workspaces` | List workspaces |
| `POST /api/conversations/{id}/messages` | Send chat message |
| `POST /api/conversations/{id}/inject-memory` | Inject memory context |
| `POST /api/memories/search` | Search memories |
| `GET /api/models/available` | List connected AI models |

## 🔐 Security

- JWT authentication with refresh tokens
- Fernet encryption for API keys at rest
- CORS configuration
- Input validation and sanitization
- SQL injection prevention via Django ORM

## 🎨 Screenshots

The interface features a cyberpunk-inspired design with:
- Neon green accents on dark backgrounds
- Angular frames and glowing borders
- Interactive 3D brain for model selection
- Responsive design for all screen sizes

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 👥 Team

Built for **CodeCraze Hackathon** by:
- [ahammadshawki8](https://github.com/ahammadshawki8)
- [mumtio](https://github.com/Mumtio)

---

**Chimera Protocol**: Unifying AI, one model at a time. 🧠⚡
