# Architecture.md

# Personal Portfolio Website - Technical Architecture

Version: 1.0

---

# Purpose

This document defines the technical architecture for the Personal Portfolio Website. It complements PRD.md and serves as the engineering blueprint for implementation.

---

# Architecture Principles

- Modular and component-driven
- Strong TypeScript typing
- Content separated from presentation
- Reusable UI components
- Mobile-first responsive architecture
- SEO-first routing
- Future-ready for blog, CMS and AI chatbot

---

# High-Level Architecture

```
Browser
   │
React + TypeScript
   │
Routing (React Router)
   │
Layouts
   │
Pages
   │
Reusable Components
   │
Typed Data Layer
```

---

# Directory Structure

```
portfolio/
├── docs/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── common/
│   │   ├── layout/
│   │   ├── sections/
│   │   └── project/
│   ├── data/
│   ├── hooks/
│   ├── layouts/
│   ├── pages/
│   ├── routes/
│   ├── styles/
│   ├── types/
│   ├── utils/
│   ├── App.tsx
│   └── main.tsx
```

---

# Routing

/ -> Home

/projects/:slug -> Case Study

/resume -> Resume Preview

Architecture must allow future routes:

/blog

/chat

/admin

---

# Data Layer

All business content resides in src/data.

Recommended files:

- profile.ts
- projects.ts
- experience.ts
- skills.ts
- certifications.ts
- social.ts
- seo.ts

Components never hardcode content.

---

# Component Hierarchy

App
 ├── Header
 ├── HomePage
 │    ├── Hero
 │    ├── About
 │    ├── Skills
 │    ├── Experience
 │    ├── Certifications
 │    ├── FeaturedProjects
 │    ├── Contact
 │    └── Footer
 └── ProjectPage

---

# Shared Components

- Section
- Container
- Button
- Badge
- Card
- Chip
- Icon
- Heading

Use composition instead of duplication.

---

# State Management

Local React state by default.

Context API only for shared UI state.

Avoid Redux in V1.

---

# Asset Strategy

assets/
- images/
- icons/
- illustrations/

Use SVG where possible.

---

# Error Handling

- 404 page
- Invalid project slug
- Contact submission failure
- Image fallback

---

# Performance

- Route lazy loading
- Dynamic imports
- Optimized images
- Tree shaking
- Code splitting

---

# Security

- Environment variables
- No secrets in frontend
- Input validation
- EmailJS keys via env

---

# Testing Strategy

- Manual responsive testing
- Accessibility audit
- Lighthouse audit
- Cross-browser validation

---

# Deployment

GitHub
    ↓
Vercel Preview
    ↓
Production

Every pull request should generate a preview deployment.

---

# Future Expansion

Architecture should support:

- Blog
- AI Chatbot
- CMS
- External project deployments
- Analytics dashboard

No breaking structural changes should be required.

---
End of Architecture.md
