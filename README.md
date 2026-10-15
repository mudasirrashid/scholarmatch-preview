<div align="center">

# 🎓 ScholarMatch

### Intelligent Scholarship Companion & Application Intelligence Platform

**The intelligent scholarship companion that finds the opportunities a student is actually eligible for — and guides them from discovery to application.**

[![Next.js](https://img.shields.io/badge/Next.js-App%20Router-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.x-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Managed-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Vercel](https://img.shields.io/badge/Vercel-Deployed-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com)

[![Status](https://img.shields.io/badge/status-production-brightgreen?style=flat-square)](https://www.scholarmatch.me)
[![License](https://img.shields.io/badge/license-Proprietary%20%2F%20All%20Rights%20Reserved-red?style=flat-square)](#-repository-notice)

### 🔗 Live Production Platform → **[https://www.scholarmatch.me](https://www.scholarmatch.me)**

</div>

---

## 📖 Table of Contents

| # | Section |
|:-:|:--------|
| 1 | [Mission & Vision](#-mission--vision) |
| 2 | [Executive Architecture & Core Loop](#-executive-architecture--core-loop) |
| 3 | [The Intelligence Core — Matching Engine v1](#-the-intelligence-core--matching-engine-v1) |
| 4 | [Technical & Backend Architecture](#-technical--backend-architecture) |
| 5 | [Application Intelligence & Workflow](#-application-intelligence--workflow) |
| 6 | [Platform Preview & UI Walkthrough](#-platform-preview--ui-walkthrough) |
| 7 | [Repository Notice](#-repository-notice) |

---

## 🎯 Mission & Vision

> **Core Philosophy**
>
> *"The intelligent scholarship companion that finds the opportunities a student is actually eligible for — and guides them from discovery to application."*

**ScholarMatch** was built to solve a structurally broken problem in global education access: talented students miss life-changing funding opportunities not because they lack merit, but because discovery is fragmented, eligibility is opaque, and the application journey is overwhelming.

ScholarMatch replaces the noise of scattered listings and Facebook groups with a **deterministic, explainable, eligibility-first matching engine** wrapped in a production-grade application workspace. Every recommendation is grounded in the student's real profile — field of study, degree level, academic record, nationality, language proficiency, and experience — so students spend their energy applying, not guessing.

### Guiding Principles

| Principle | What It Means in Practice |
|:----------|:--------------------------|
| **Eligibility First** | Never surface an opportunity a student cannot win. Hard gates filter before ranking ever occurs. |
| **Explainability over Black Box** | Every match ships with a transparent "Why you match" breakdown and a single highest-leverage "One thing to improve." |
| **Discovery → Application Continuity** | Matching is not the product. The product is the guided journey from match to submitted application. |
| **Trust by Design** | Verified data workflows, transparent disclaimers, and secure-by-default session handling. |
| **Cinematic but Purposeful** | Delightful interface, but every animation and glass surface serves comprehension and confidence. |

---

## 🏛️ Executive Architecture & Core Loop

ScholarMatch is architected as a **closed-loop student intelligence system**. Each stage feeds verified signal back into the next, so the platform compounds in accuracy and usefulness the longer a student uses it.

### The ScholarMatch Core Loop

```text
┌──────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   Profile  ──►  Match  ──►  Understand  ──►  Prepare  ──►  Apply          │
│      ▲                                                        │          │
│      │                                                        ▼          │
│      └────────────────  Return  ◄──  Track  ◄─────────────────┘          │
│                                                                          │
│   Intelligent feedback loop: every interaction refines future matches.   │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

| Stage | Description |
|:------|:------------|
| **Profile** | Structured capture of academic, personal, eligibility, and preference signals. |
| **Match** | Deterministic weighted scoring across 7 dimensions produces a ranked, gated shortlist. |
| **Understand** | Explainable breakdown clarifies *why* each opportunity fits and *what* to improve. |
| **Prepare** | Document checklists and preparatory guidance surface exactly what is required. |
| **Apply** | Step-by-step application tracker guides execution from eligibility check to submission. |
| **Track** | Status pipeline gives complete visibility across every active application. |
| **Return** | Verified outcomes and evolving profiles feed back to sharpen the next match cycle. |

### Dual-Sided System Architecture

ScholarMatch is intentionally split into two surfaces with distinct design languages and responsibilities.

#### 🌐 Public Side — Cinematic Discovery Engine

A high-conversion, immersive surface designed for first-time visitors and organic discovery.

- **Cinematic Discovery Engine** — motion-driven, glassmorphic landing experience that communicates value in seconds.
- **Intelligent Filter System** — instant filtering across the dimensions that matter most:
  - 🎓 **Fully Funded**
  - 🎓 **Undergraduate**
  - 🎓 **Masters**
  - 🎓 **PhD**
  - 🌍 **Country-Specific**
- **SEO-Optimized Opportunity Surface** — server-rendered, crawlable scholarship discovery.
- **Conversion Funnel** — clear path from discovery → sign-up → personalized matching.

#### 🎒 Student Side — Personalized Application Workspace

An authenticated, personalized intelligence hub where matching and the application lifecycle live.

| Route | Purpose |
|:------|:--------|
| `/dashboard` | Command center — match summary, application pipeline, deadlines, and next actions. |
| `/matches` | Ranked, eligibility-gated opportunities with explainable scoring. |
| `/applications` | Full lifecycle tracker across every active submission. |
| `/documents` | Centralized document vault and readiness checklist. |
| `/saved` | Curated shortlist of opportunities flagged for deeper review. |
| `/ai-assistant` | Conversational guidance layer across discovery, prep, and application strategy. |

---

## 🧠 The Intelligence Core — Matching Engine v1

At the heart of ScholarMatch is a **deterministic, weighted matching algorithm (v1)**. It is deliberately rule-based and transparent rather than an opaque model — because a student's future should never depend on a score they cannot understand or contest.

### Two-Phase Engine: Gate, Then Rank

```text
┌──────────────────────────────────────────────────────────────────────────┐
│  PHASE 1 — ELIGIBILITY GATE (Hard Filter)                                │
│  Non-negotiable criteria: nationality/eligibility, degree level,         │
│  deadline & status. Ineligible opportunities are removed entirely.       │
└──────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
┌──────────────────────────────────────────────────────────────────────────┐
│  PHASE 2 — WEIGHTED SCORING (Ranking)                                    │
│  Eligible opportunities scored across 7 weighted dimensions.            │
└──────────────────────────────────────────────────────────────────────────┘
```

### Weighted Scoring Breakdown

| # | Dimension | Weight | What It Evaluates |
|:-:|:----------|:------:|:------------------|
| 1 | **Field** | **25%** | Alignment between the student's field of study and the scholarship's target disciplines. |
| 2 | **Degree** | **20%** | Degree-level fit (Undergraduate / Masters / PhD) between profile and opportunity. |
| 3 | **Academic / GPA** | **20%** | Academic performance against opportunity expectations and competitiveness bands. |
| 4 | **Nationality / Eligibility Gate** | **15%** | Citizenship, residency, and program-specific eligibility constraints. |
| 5 | **Language / IELTS / TOEFL** | **10%** | Language proficiency alignment with program requirements. |
| 6 | **Experience** | **5%** | Relevant experience, projects, and background. |
| 7 | **Preferences** | **5%** | Student-stated preferences (location, funding type, study mode, priorities). |
|   | **Total** | **100%** | |

```text
Match Score = Σ ( dimension_scoreᵢ × weightᵢ )   for i = 1 … 7
```

> **Design note:** Field and Degree together account for **45%** of the score — reflecting the reality that discipline and level alignment are the strongest predictors of a meaningful, actionable match.

### Explainable AI Matching

University and scholarship discovery platforms historically behave as black boxes. ScholarMatch refuses that. Every ranked result renders a **human-readable rationale** with two explicit indicators:

<table>
<tr>
<th align="left">✅ Why You Match</th>
<th align="left">🎯 One Thing To Improve</th>
</tr>
<tr>
<td valign="top">

A transparent breakdown of the weighted dimensions where the student is strong — e.g. *field alignment, degree fit, GPA band, nationality eligibility* — so the score is never a mystery.

</td>
<td valign="top">

The **single highest-leverage** dimension the student can realistically improve to unlock stronger matches or more competitive positioning — actionable, focused, and non-overwhelming.

</td>
</tr>
</table>

This transforms the engine from a filter into a **coach** — turning every match into an opportunity to become a stronger candidate.

---

## 🏗️ Technical & Backend Architecture

### Frontend

| Layer | Technology | Role |
|:------|:-----------|:-----|
| **Framework** | **Next.js (React) — App Router** | Server-first rendering, streaming, nested layouts, SEO-critical public surfaces. |
| **Language** | **TypeScript** | End-to-end type safety across components, data models, and engine inputs. |
| **Styling** | **Tailwind CSS** | Utility-first design system with a consistent token set. |
| **Motion** | **Framer Motion** | Purposeful micro-interactions, page transitions, and the glassmorphic UI design system. |
| **Design System** | **Glassmorphism** | Layered translucency, depth, and cinematic polish — used purposefully to guide attention. |

### Backend & Database

| Layer | Technology | Role |
|:------|:-----------|:-----|
| **Backend Platform** | **Supabase** | Auth, database, and realtime primitives. |
| **Database** | **Managed PostgreSQL** | Relational core for profiles, opportunities, and applications. |
| **Security Model** | **Row Level Security (RLS)** | Every table is policy-guarded; users can only ever read/write their own rows. |
| **Data Integrity** | **Automated Triggers** | Profile synchronization, `updated_at` maintenance, and derived records kept consistent at the database layer. |
| **Sessions** | **Supabase Auth** | Secure, token-based session handling with protected routes. |

### Security & Trust

- **Row Level Security First** — authorization is enforced in the database, not just the application, eliminating entire classes of data-leak risk.
- **Automated Data Verification Workflows** — structured verification of opportunity data and eligibility constraints before it reaches a student.
- **Transparent Eligibility Disclaimers** — the platform never overstates certainty; eligibility is always presented as guidance, with the official source of truth being the scholarship provider.
- **Secure Session Handling** — Supabase Auth manages authentication and session lifecycle with protected server and client routes.
- **Least-Privilege Data Access** — students read and write only what belongs to them; public discovery data is served from a separate, read-scoped path.

---

## 🚀 Application Intelligence & Workflow

Matching is only half the mission. ScholarMatch operationalizes the entire application journey through a **step-by-step tracker** and **interactive document checklists**.

### The Application Journey Tracker

```text
 01 Check Eligibility  →  02 Gather Documents  →  03 Draft Essays  →  04 Collect Recommendations
         │
         ▼
 05 Review Requirements →  06 Final QA  →  07 Submit  ✅
```

| Step | Stage | Student Outcome |
|:----:|:------|:----------------|
| **01** | **Check Eligibility** | Confirm hard requirements are met before investing effort. |
| **02** | **Gather Documents** | Know exactly which documents are required and where they stand. |
| **03** | **Draft Essays** | Prepare motivation statements and core written materials. |
| **04** | **Collect Recommendations** | Track recommender requests through to completion. |
| **05** | **Review Requirements** | Validate every program-specific rule before final assembly. |
| **06** | **Final QA** | Last-pass completeness and consistency check. |
| **07** | **Submit** | Confidently submit — with full visibility of what's done and what remains. |

### Interactive Document Checklists

Each opportunity exposes a dynamic, per-application checklist so readiness is always unambiguous:

- 🛂 **Passport / ID**
- 📜 **Academic Transcripts**
- 📄 **CV / Résumé**
- ✍️ **Motivation / Statement of Purpose Letter**
- 💌 **Recommendation Letters**
- 🌐 **Language Test Scores (IELTS / TOEFL)**
- 🧾 **Additional Program-Specific Documents**

Checklist state is persisted per application, giving students a single source of truth for readiness across every opportunity they pursue.

---

## 📸 Platform Preview & UI Walkthrough

> **Status:** Screenshots and cinematic UI walkthrough captures are being prepared. Image placeholders below map to the `./screenshots/` directory in this repository.

| Surface | Description | Preview |
|:--------|:------------|:--------|
| **Cinematic Landing** | Public discovery engine with glassmorphic hero and motion-driven storytelling. | ![Landing](./screenshots/landing.png) |
| **Filter System** | Fully Funded / Undergraduate / Masters / PhD / Country-specific instant filtering. | ![Filters](./screenshots/filters.png) |
| **Dashboard** | Personalized command center with match summary and application pipeline. | ![Dashboard](./screenshots/dashboard.png) |
| **Matches** | Ranked, eligibility-gated opportunities with explainable scoring. | ![Matches](./screenshots/matches.png) |
| **Explainable Match Card** | "Why you match" vs "One thing to improve" breakdown. | ![Match Card](./screenshots/match-card.png) |
| **Applications Tracker** | 7-step application journey from Check Eligibility → Submit. | ![Applications](./screenshots/applications.png) |
| **Documents Vault** | Interactive document checklist and readiness tracking. | ![Documents](./screenshots/documents.png) |
| **Saved Opportunities** | Curated shortlist for deeper review. | ![Saved](./screenshots/saved.png) |
| **AI Assistant** | Conversational guidance across discovery, prep, and strategy. | ![AI Assistant](./screenshots/ai-assistant.png) |

_Screenshot assets will be added to [`./screenshots/`](./screenshots/) and this table will render the live captures._

---

## 🔒 Repository Notice

> **This repository is the public architectural portfolio and documentation hub for ScholarMatch.**
>
> The core source code — including the full implementation of the matching engine, application logic, and backend services — **remains protected in a private repository** and is intentionally **not** published here.
>
> This preview repository exists to:
> - Document the **architecture, intelligence model, and product vision** of ScholarMatch.
> - Provide a **professional reference** for the platform's design and engineering decisions.
> - Serve as a **portfolio artifact** demonstrating enterprise-grade EdTech system design.
>
> For collaboration, investment, or technical inquiries, please reach out via the live platform: **[https://www.scholarmatch.me](https://www.scholarmatch.me)**

**© ScholarMatch. All rights reserved.** — Proprietary. No part of the ScholarMatch product, brand, or underlying intellectual property may be reproduced or redistributed without explicit written permission.

---

<div align="center">

**ScholarMatch** — from discovery to application, intelligently.

🔗 **[www.scholarmatch.me](https://www.scholarmatch.me)**

</div>
