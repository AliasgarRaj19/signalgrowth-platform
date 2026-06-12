# ⚡ SignalGrowth — AI Operating System Platform

> A production-grade, multi-tenant AI SaaS platform built from the ground up — featuring full authentication, RBAC, OpenAI GPT-4o integration, LangChain orchestration, and private VPS infrastructure. No Zapier. No Make. No third-party automation. Complete data ownership.

**Live Platform:** [app.signalgrowth.in](https://app.signalgrowth.in) &nbsp;|&nbsp; **Website:** [signalgrowth.in](https://signalgrowth.in)

---

## 🧠 What Is SignalGrowth?

SignalGrowth is an **AI-powered business operating system** — a shared platform that hosts multiple AI systems, each solving a specific business domain problem. Think of it as the infrastructure layer that allows AI agents, workflow engines, and business logic to run reliably in production.

Built entirely solo by one developer. Every line of architecture, every API, every deployment decision — owned end to end.

---

## 🏗️ Platform Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                     SIGNALGROWTH PLATFORM                       │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                    FRONTEND LAYER                       │   │
│  │              Next.js + React                            │   │
│  │   Role-Based Dashboards │ Onboarding Flows │ UI         │   │
│  └──────────────────────────┬──────────────────────────────┘   │
│                             │                                   │
│  ┌──────────────────────────▼──────────────────────────────┐   │
│  │                    API GATEWAY                          │   │
│  │              Node.js + Express.js                       │   │
│  │         REST APIs │ JWT Validation │ RBAC               │   │
│  └────────┬──────────────────────────────┬─────────────────┘   │
│           │                              │                      │
│  ┌────────▼──────────┐       ┌───────────▼──────────────────┐  │
│  │  AUTH & IDENTITY  │       │      AI INTEGRATION LAYER    │  │
│  │                   │       │                              │  │
│  │ Registration      │       │  Provider Abstraction Layer  │  │
│  │ Email Verification│       │  OpenAI GPT-4o               │  │
│  │ JWT Tokens        │       │  LangChain Orchestration     │  │
│  │ Password Reset    │       │  Message Routing             │  │
│  │ RBAC              │       │  Agent Extension Hooks       │  │
│  │ Multi-Tenant ISO  │       │  Memory Context Manager      │  │
│  └────────┬──────────┘       └───────────┬──────────────────┘  │
│           │                              │                      │
│  ┌────────▼──────────────────────────────▼──────────────────┐  │
│  │                    DATA LAYER                            │  │
│  │                   PostgreSQL                             │  │
│  │  Users │ Companies │ Roles │ Plans │ Storage Tracking   │  │
│  │  AI Context │ Workflow State │ Audit Logs               │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                 │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                 BUSINESS SYSTEMS                         │  │
│  │                                                          │  │
│  │  ┌────────────┐  ┌────────────┐  ┌────────────────────┐ │  │
│  │  │  Sales OS  │  │   HR OS    │  │  Content Intel OS  │ │  │
│  │  └────────────┘  └────────────┘  └────────────────────┘ │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                    INFRASTRUCTURE                               │
│         Private VPS │ PM2 │ NGINX │ CI/CD │ SSL                │
└─────────────────────────────────────────────────────────────────┘
```

---

## ⚙️ Platform Components

### Authentication & Identity
- User registration with email verification
- JWT-based session management with refresh token flow
- Password reset via time-limited email tokens
- Multi-level RBAC (Super Admin / Company Admin / Manager / User)
- Tenant isolation — each company's data fully separated

### AI Integration Layer
- **Provider abstraction layer** — swap AI models without changing business logic
- Currently powered by **OpenAI GPT-4o**
- Real-time message routing with backend LLM orchestration
- **LangChain-based orchestration** for multi-step agent workflows
- Extensible agent architecture — new agents plug in without platform changes
- Memory context manager for persistent, grounded AI conversations

### Multi-Tenant SaaS Architecture
- Individual users and company accounts on a shared infrastructure
- Role-based dashboard experiences per tenant type
- Subscription and plan management layer
- Storage governance tracking per tenant

### Storage & Document Management
- Document architecture supporting AI-assisted workflows
- Candidate records and recruitment history
- Future knowledge system integration hooks

### Infrastructure
- Deployed on **private VPS** — complete data ownership
- **PM2** for process management and zero-downtime restarts
- **NGINX** reverse proxy with SSL termination
- CI/CD pipeline for automated deployments
- System monitoring and alerting

---

## 🛠️ Full Tech Stack

| Category | Technology |
|----------|-----------|
| Frontend | Next.js, React |
| Backend | Node.js, Express.js |
| Database | PostgreSQL |
| AI Model | OpenAI GPT-4o |
| AI Orchestration | LangChain |
| Auth | JWT, RBAC, Email Verification |
| Infrastructure | Private VPS, PM2, NGINX |
| Deployment | CI/CD Pipelines |
| Architecture | Multi-Tenant SaaS |

---

## 🚀 AI Systems Built on This Platform

| System | What It Does | Demo |
|--------|-------------|------|
| [Sales OS](https://github.com/AliasgarRaj19/signalgrowth-sales-os) | Full lead lifecycle, pipeline management, AI sales agent | [YouTube](https://youtu.be/zaRG07H0aaY) |
| [HR Recruitment OS](https://github.com/AliasgarRaj19/signalgrowth-hr-os) | Resume parsing, candidate matching, employee tracking, payroll | [YouTube](https://youtube.com/watch?v=EpdX-zrn6d4) |
| Content Intelligence OS | AI content generation using competitor intelligence + brand context | Coming soon |
| AI Chat CRM | Memory-driven conversational CRM with full sales lifecycle | [YouTube](https://youtu.be/_q9W6H_6KgQ) |

---

## 🔒 Design Principles

**Data Ownership First**
All data lives on a private VPS. No third-party storage, no shared databases. Clients own their data completely.

**No Third-Party Automation Dependency**
Every workflow, business rule, and automation runs on a dedicated backend. No Zapier, no Make, no n8n. Faster execution, lower cost, full control.

**Hallucination-Free AI**
AI responses are bound to structured stored data. The AI cannot fabricate information — it can only surface what is actually in the database.

**LangGraph-Ready Architecture**
Extension hooks are built into the platform for future multi-agent orchestration, autonomous workflows, and predictive intelligence layers.

---

## 📋 Roadmap

- [x] Multi-tenant authentication and RBAC
- [x] AI integration layer with provider abstraction
- [x] Sales Operating System
- [x] HR Recruitment Operating System
- [x] Content Intelligence System
- [x] AI Chat CRM
- [ ] LangGraph multi-agent orchestration
- [ ] RAG pipeline integration (pgvector)
- [ ] Predictive analytics layer
- [ ] Mobile dashboard

---

## 👤 Built By

**Aliasgar Raj** — AI Systems Builder & Founder, SignalGrowth

Sole designer, developer, and operator of this platform. 14+ years of business operations experience in e-commerce, sales, HR, and digital marketing — all channelled into building AI systems that solve the exact problems those domains face.

- 🌐 [signalgrowth.in](https://signalgrowth.in)
- 💼 [linkedin.com/in/aliasgarraj](https://linkedin.com/in/aliasgarraj)
- 📧 askaliasgarnow@gmail.com
- 🐙 [github.com/AliasgarRaj19](https://github.com/AliasgarRaj19)

> *Available for consulting engagements, full-time AI/technical roles, and custom SaaS builds.*
