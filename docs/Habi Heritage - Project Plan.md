Habi Heritage - Project Plan
Version 1.0
Date: 2025-10-12
Prepared by: Project Team (SE2)

A. PROJECT OVERVIEW
- Purpose: Habi Heritage is a web platform that showcases and sustains Filipino weaving traditions through storytelling, galleries, fundraising/donations, and an e-commerce storefront for artisan products.
- Background: To ensure sustainable livelihoods for artisans and preserve cultural heritage, the platform integrates content (stories, short films), community support (donations, fundraising), and commerce.
- Expected benefits:
  - Economic empowerment of partner artisans via online sales and donations
  - Increased public awareness through multimedia storytelling and galleries
  - Operational efficiency via an integrated CMS and admin dashboard

B. PROJECT OBJECTIVES
- Launch MVP web application with core modules (Catalog, Checkout/Donations, Gallery, Storytelling, Admin) within 10 weeks.
- Achieve < 2.5s median page load on 4G for key pages (Home, Product, Checkout).
- Enable secure payments/donations with 99.9% payment gateway uptime (via provider SLA).
- Publish at least 20 catalog items, 12 gallery assets, and 6 stories/short films at launch.
- Attain 80%+ positive stakeholder satisfaction in post-launch survey.

C. SCOPE OF THE PROJECT
- In scope (MVP):
  - User authentication (register/login), profile
  - Product catalog, cart, checkout, orders; donations/fundraising module
  - Storytelling and short-film publishing; image/video gallery
  - Admin dashboard for content, products, orders, donations
  - Responsive web (desktop/mobile), accessibility baseline (WCAG AA basics)
  - Backend APIs (Laravel), Frontend SPA (React)
- Out of scope (Phase 1):
  - Native mobile apps (iOS/Android)
  - Multi-vendor marketplace, vendor onboarding/settlement
  - Advanced personalization/AI recommendations
  - Internationalization beyond English/Filipino baseline
- Assumptions:
  - Payment processor account (e.g., Stripe/PayPal) available and approved
  - Initial content (stories, media, product data) provided before UAT
  - Hosting with staging and production environments provisioned by Week 6
- Constraints:
  - Fixed 10-week MVP timeline; limited student team availability
  - Budget cap aligned to coursework; prefer open-source tooling

D. PROJECT DELIVERABLES
- Documentation: Project Charter, SRS, Architecture & API spec, Test Plan and Reports, Deployment Guide, Admin User Guide
- Design: Low/high-fidelity wireframes, UI kit, clickable prototype
- Implementation: Laravel backend, React frontend, MySQL schema, seed data
- Operations: CI workflow, staging/prod deployments, monitoring baseline
- Final handover: Source code repository, credentials inventory, training session

E. WORK BREAKDOWN STRUCTURE (WBS)
- Level 1: Habi Heritage MVP
- Level 2 and sample Level 3 work packages:
  1) Initiation
     - Stakeholder register, Project Charter, Kickoff
  2) Planning
     - Scope statement, WBS, Schedule (Gantt/CPM), Risk Register, Communication plan
  3) UX/UI Design
     - Research, IA, Wireframes, Hi-fi mockups, Design system
  4) Backend (Laravel)
     - Models (Product, Donation, Fundraising, Gallery, Storytelling, User)
     - REST APIs (auth, catalog, cart/checkout, donations, content)
     - Payments integration, Validation, Logging, Seeders
  5) Frontend (React)
     - App shell, Routing, Auth, Catalog, Cart/Checkout, Donations, Gallery, Storytelling, Admin
     - API client, State management, Responsive layout, Accessibility pass
  6) Data & Content
     - Schema/migrations, Sample data, Content loading, Media optimization
  7) Integration
     - End-to-end flows, Error handling, Performance tuning
  8) QA
     - Test plan, Unit tests (PHPUnit/Jest), E2E (Cypress/Playwright), UAT
  9) Deployment
     - Staging, Prod, Rollback plan, Monitoring/alerts
  10) Training & Handover
     - Admin training, Guides, Knowledge transfer
  11) Project Management
     - Status reports, Risk/Change logs, CCB decisions

F. PROJECT SCHEDULE (TIMELINE)
- Approach: Gantt chart with CPM; dependencies primarily Finish-to-Start from Planning → Design → Backend/Frontend → Integration → QA → Deployment.
- Summary timeline (10 weeks, Week 1 = project start):
  - W1: Initiation (Charter, kickoff); Planning (scope, WBS, schedule, risk)
  - W2–W3: UX/UI Design; Backend scaffolding; Frontend setup (SS dependencies)
  - W3–W6: Backend feature development (APIs, payments); Frontend feature development (pages/components)
  - W5–W6: Data/content preparation; media pipeline
  - W6–W7: Integration and stabilization; performance pass
  - W7–W8: QA (unit, integration, E2E), bug fixes; UAT prep
  - W9: UAT with stakeholders; release candidate
  - W10: Production deployment; training; project closure
- Key milestones:
  - M1: Charter approved (end W1)
  - M2: Design sign-off (end W3)
  - M3: Feature complete (end W6)
  - M4: UAT sign-off (end W9)
  - M5: Go-live (W10)

G. RESOURCE PLANNING
- Team roles (MVP):
  - Project Manager (part-time)
  - Technical Lead / Full-stack Engineer
  - Backend Developer (Laravel)
  - Frontend Developer (React)
  - QA Engineer
  - UI/UX Designer (part-time)
- Tools/Technologies:
  - Frontend: React, Vite/CRA, CSS Modules/Tailwind
  - Backend: Laravel, PHP 8.x, Sanctum/Auth, PHPUnit
  - Database/Storage: MySQL/MariaDB, S3-compatible object storage
  - Payments/Donations: Stripe/PayPal integration
  - DevOps: GitHub, CI, Docker (optional), Apache/Nginx on Linux
  - PM/Collaboration: Trello/Jira, Figma, Slack/Teams, Google Drive
  - Testing: Jest/RTL, Cypress/Playwright, Postman
- Environments:
  - Development (local), Staging (feature/UAT), Production (HA backups)

H. BUDGET AND COST ESTIMATION
- Estimation approach: Bottom-up WBS-based with Three-Point (PERT) on uncertain tasks; 10% contingency informed by qualitative risk analysis and EMV.
- Effort estimate (illustrative):
  - PM: 10 h/week × 10 weeks = 100 h
  - UX: 10 h/week × 4 weeks = 40 h
  - Backend: 30 h/week × 10 weeks = 300 h
  - Frontend: 30 h/week × 10 weeks = 300 h
  - QA: 15 h/week × 6 weeks = 90 h
  - Integration/DevOps: 2 h/week × 10 weeks = 20 h
  - Total base effort ≈ 850 h
- Cost model (example, blended rate ₱700/hour):
  - Base cost: 850 h × ₱700 ≈ ₱595,000
  - Contingency (10%): ≈ ₱59,500
  - Total estimated budget (ROM): ≈ ₱655,000
  - Accuracy expectation: Budget estimate phase (−15% to +25%) per SE2 guidance
- Major cost buckets:
  - Development = ~55%
  - Design = ~7%
  - QA/UAT = ~15%
  - DevOps/Hosting (12 months) = ~10%
  - PM/Overheads = ~13%

Planning and Estimation Notes (from SE2 lessons)
- Use WBS for decomposition and bottom-up estimates; track via Gantt and CPM.
- Identify risks early; maintain a Risk Register; apply qualitative prioritization and add buffers based on EMV where applicable.
- Control scope creep through formal change requests and a simple CCB; update schedule/budget baselines upon approved changes.

References
- CSP113 Week 4 — Project Planning & Estimation 1
- CSP113 Week 5 — Project Planning & Estimation 2
- Project Planning Outline