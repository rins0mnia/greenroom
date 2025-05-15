# GREENROOM

**Greenroom** is a modular Creator OS for streamers, VTubers, and digital-native teams—blending content management, AI task orchestration, and brand infrastructure into one intelligent platform. It functions as a hybrid between a **CRM, campaign planner, and Chief of Staff**, purpose-built for the creator economy.

---

## ✨ Vision

Modern creators run digital businesses—but lack the infrastructure to operate like one.

Greenroom gives creators and orgs a **centralized system** to manage:
- Campaign pipelines
- Brand assets
- AI-powered workflows
- Cross-platform analytics
- and intelligent support via **Kira**, your built-in Chief of Staff agent.

---

## 🧠 Agent Architecture

Kira is not just an LLM wrapper—she is Greenroom’s central command system.

Every user request (from scheduling to content generation) flows through Kira, who:
- Holds context over time
- Routes tasks to sub-agents (e.g., Aura for content, Clove for learning)
- Executes tools, APIs, and prompts as needed
- Responds with high-context, structured outputs

Built with **LangChain**, Kira uses a modular toolset and router-based logic to power workflows, automate suggestions, and assist creator teams in real-time.

---

## 🛠️ Tech Stack

| Layer         | Stack                             | Purpose                          |
|---------------|------------------------------------|----------------------------------|
| Frontend      | Next.js + Tailwind CSS             | Modern UI dashboard              |
| Backend       | FastAPI (Python)                   | API & agent routing              |
| Auth          | Supabase Auth                      | Secure login & JWT               |
| Database      | Supabase Postgres                  | Content, users, memory storage   |
| AI Orchestration | LangChain + OpenAI APIs         | Kira & agent logic               |
| File Storage  | Supabase Storage                   | Uploads and brand assets         |
| Deployment    | Vercel (frontend) + Fly.io/Render  | Hosting & CI/CD                  |
| Monitoring    | Sentry, Supabase logs              | Logging & debugging              |
| Queueing (TBD)| Redis + Celery or Edge Functions   | Async agent tasks                |

---

## 🧱 System Architecture

```plaintext
[Frontend: Next.js]
        ↓
[API Layer: FastAPI]
        ↓
[Kira: LangChain Router Agent]
        ↓             ↓             ↓
[Aura]        [Clove]        [Custom Tools]
        ↓             ↓             ↓
[Supabase: DB / Auth / Storage]
