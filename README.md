# 🎓 ScholarMatch | AI-Powered Fully Funded Scholarship Platform

> **"The intelligent scholarship companion built by an AI Engineer — designed to find the exact opportunities students are eligible for, eliminating the chaos of international funding searches."**

🌐 **Live Production App:** [scholarmatch.me](https://www.scholarmatch.me)

---

## 🧠 Mission & Platform Overview
International students face massive friction finding fully funded scholarships due to fragmented data, complex eligibility criteria, and generic search engines. ScholarMatch solves this by acting as an **intelligent companion**—matching a student's exact academic profile, GPA, and background against global opportunities using deterministic AI logic, and guiding them step-by-step from discovery to application submission.

**Core Lifecycle Loop:**  
`Profile` → `Match` → `Understand` → `Prepare` → `Apply` → `Track` → `Return`

---

## 🏗️ Dual-Sided Platform Architecture

- **Public Side (Cinematic Discovery Engine):**
  - High-performance exploration hub with advanced filtering systems (Fully Funded, Undergraduate, Masters, PhD, Country-specific).
  - Modern, responsive landing experience with live interactive elements.
- **Student Side (`/dashboard` & Workspace):**
  - Dedicated student control centers: `/dashboard`, `/matches`, `/applications`, `/documents`, `/saved`, and `/ai-assistant`.

---

## 🤖 The Intelligence Core (Matching Engine v1)

Going far beyond simple keyword filters, ScholarMatch runs a precision weighted multi-dimensional scoring matrix:
- **Field of Study:** 25%
- **Degree Level:** 20%
- **Academic / GPA:** 20%
- **Nationality / Eligibility Gate:** 15%
- **Language Requirements (IELTS/TOEFL):** 10%
- **Experience & Projects:** 5%
- **Student Preferences:** 5%

**Explainable AI Matching:** Provides clear breakdown metrics indicating **"Why you match"** vs **"One thing to improve"** (e.g., live 96% match indicators with interactive bubble and glow effects).

---

## 🛠️ Technical & Backend Stack

- **Frontend:** Next.js (App Router), React, TypeScript, Tailwind CSS, Framer Motion (Glassmorphic UI with custom bubble/glow micro-interactions).
- **Backend & Database:** Supabase (Managed PostgreSQL), Row Level Security (RLS) policies, and automated database triggers for user profile synchronization.
- **Security & Trust:** Strict session handling via Supabase Auth, transparent eligibility disclaimers, and data verification workflows.

---

## 🎯 Application Intelligence & Workflow

- **Step-by-Step Journey Tracker:** Breaks down the overwhelming application process into 7 clear milestones:
  `01 Check Eligibility` → `02 Prepare Documents` → `03 Create Account` → `04 Complete Application` → `05 Upload Documents` → `06 Review` → `07 Submit`.
- **Interactive Document Checklists:** Built-in tracking for passports, transcripts, CVs, and motivation/recommendation letters.

---

## 📸 Platform Preview & UI Walkthrough

*(Upload your site screenshots here into the `./screenshots/` folder)*

| AI Discovery & Matching | Application Journey Tracker |
| :---: | :---: |
| ![Matching Engine](./screenshots/matching.png) | ![Tracker](./screenshots/tracker.png) |

---

## 🛡️ Repository Notice & Academic Integrity
This repository serves as the public architectural showcase and documentation hub for **ScholarMatch**. The core source code, proprietary database schemas, and AI matching pipelines remain hosted in a private repository for security and intellectual property protection.
