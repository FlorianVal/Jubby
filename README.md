# Jubby

Don't Apply. Just Swipe. Let Jubby handle the paperwork.

## 🚀 Vision
**"Stop searching, start swiping."**
Jubby is a mobile-first web application designed to eliminate the friction of job hunting. It uses a "Tinder-like" interface to browse curated job offers. When a user "swipes right," an autonomous AI Agent takes over to:
1. Generate a hyper-personalized CV and Cover Letter.
2. Navigate to the company's portal.
3. Automatically fill out the application form and upload documents.

## 🏗 Architecture Overview
This project follows a **Hybrid Monorepo** structure.
- **Frontend:** Next.js (React) for a responsive PWA interface.
- **Backend:** FastAPI (Python) for the REST API.
- **Workers:** Celery + Redis for asynchronous AI processing and browser automation.
- **Database:** PostgreSQL (User data & Jobs) + S3 (Document storage).

## 🛠 Tech Stack
| Component | Technology | Role |
|-----------|------------|------|
| **Frontend** | Next.js 14, TailwindCSS | User Interface & State Management |
| **Backend** | Python 3.11, FastAPI | API Logic & Orchestration |
| **Async Task** | Celery, Redis | Queue management for heavy AI tasks |
| **Database** | PostgreSQL, Supabase | Data persistence |
| **AI/LLM** | OpenAI API (GPT-4o) | CV Generation & Contextual Analysis |
| **Automation** | Playwright | "Computer Use" (Browser manipulation) |

## 📦 Getting Started

### Prerequisites
- Docker & Docker Compose
- Node.js 18+
- Python 3.11+

### Installation
1. Clone the repository.
2. Create a `.env` file based on `.env.example`.
3. Run the stack:
   ```bash
   docker-compose up --build