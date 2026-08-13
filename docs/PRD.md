# Personal Portfolio Website - Engineering Product Requirements Document (PRD)

> **Version:** 1.0 (Draft)
> **Status:** In Progress
> **Author:** ChatGPT
> **Project:** Personal Portfolio Website

---

# Preface

This document is Part 1 of the complete Engineering PRD. It establishes the product vision, objectives, scope, guiding principles, and high-level requirements. Subsequent sections will be appended until the final PRD is complete.

## Executive Summary

The objective is to build a premium, modern, recruiter-focused portfolio website that positions Sakshi Jain as a professional who transforms business problems into data-driven insights and AI-powered solutions.

The portfolio will prioritize project storytelling over résumé-style content and will be optimized for recruiters, hiring managers, consulting firms, and freelance opportunities.

## Product Vision

Create a clean, elegant, high-performance portfolio that feels closer to a SaaS product than a traditional résumé website.

Core principles:
- Showcase projects first
- Tell a business impact story
- Maintain a scalable architecture
- Be optimized for future expansion (blog, AI chatbot, analytics)
- Deliver an excellent mobile and desktop experience

## Product Goals

### Primary Goals
1. Help secure Data Analyst opportunities.
2. Build a strong professional personal brand.
3. Demonstrate engineering and AI capabilities.
4. Showcase real projects and case studies.
5. Enable freelance credibility.

### Success Metrics
- Recruiters can understand value proposition within 10 seconds.
- Projects are the most-clicked section.
- Lighthouse targets:
  - Performance ≥95
  - Accessibility ≥95
  - Best Practices ≥95
  - SEO ≥95

## Target Audience

Primary:
- Recruiters
- Hiring Managers
- Data Analytics Managers
- Consulting Firms

Secondary:
- Freelance clients
- Professional peers

## Brand Positioning

Primary narrative:

> I transform business problems into data-driven insights and intelligent AI-powered solutions.

Avoid positioning as only a dashboard developer or only an AI engineer.

## Scope

### MVP (Version 1)

- Single-page portfolio
- Sticky navigation
- Hero
- About
- Skills
- Experience timeline
- Certifications
- Featured projects
- Contact section
- Individual project case-study pages
- Resume preview
- SEO optimization

### Future Versions
Version 2:
- Blog
- Visitor analytics
- Enhanced case studies

Version 3:
- AI chatbot
- CMS-driven content

---
_End of Part 1. Remaining sections will be appended._


# Functional Requirements

## Navigation
- Sticky navigation visible across all sections.
- Smooth scrolling between sections.
- Active section indicator.
- Resume opens in a new browser tab.

## Hero Section
- No profile photograph.
- Professional headline with concise value proposition.
- Primary CTA: View Projects.
- Secondary CTA: Download Resume.

## About
- Narrative-driven, concise, emphasizing business impact rather than chronology.

## Skills
Group skills into:
- Programming
- Analytics
- AI
- Development

Display subtle proficiency indicators rather than percentages.

## Experience
- Vertical timeline.
- Company names anonymized initially.
- Highlight business outcomes.

## Projects
Portfolio shall include:
- 3 Analytics projects
- 1 Power BI dashboard
- 1 Advanced Excel dashboard
- 3 AI / Development projects

Each project card includes:
- Cover image
- Title
- Description
- Technology tags
- Case Study button

## Case Study Pages

Every project follows a common template:
1. Hero
2. Overview
3. Business Problem
4. Objectives
5. Solution
6. Technology Stack
7. Screenshots
8. Results / Impact
9. GitHub
10. Live Demo

Architecture diagrams and challenge sections are intentionally excluded from V1.

# Non-Functional Requirements

## Performance
- Lighthouse >=95 across Performance, Accessibility, SEO and Best Practices.
- Images optimized and lazy loaded.
- Responsive interactions under 100ms where feasible.

## Accessibility
- WCAG 2.2 AA target.
- Keyboard navigation.
- Semantic HTML.
- Proper heading hierarchy.
- Visible focus states.

## SEO
- Metadata for every page.
- Open Graph tags.
- Structured JSON-LD.
- Sitemap.xml
- robots.txt


# Information Architecture

## Sitemap

```
/
├── Home
│   ├── Hero
│   ├── About
│   ├── Skills
│   ├── Experience
│   ├── Certifications
│   ├── Featured Projects
│   ├── Contact
│   └── Footer
├── /projects
│   └── /:slug
└── /resume
```

## Navigation

Sticky top navigation:

- About
- Skills
- Experience
- Projects
- Certifications
- Contact
- Resume

Navigation requirements:
- Smooth scrolling
- Active section highlighting
- Mobile hamburger menu
- Keyboard accessible
- Logo returns to Hero

# User Flows

## Recruiter Flow
Landing → Hero → Projects → Case Study → Resume → Contact

## Hiring Manager Flow
Landing → About → Experience → Projects → GitHub → Contact

## Freelance Client Flow
Landing → Projects → Results → Contact Form

# Content Strategy

Priority order:
1. Demonstrate business impact
2. Showcase projects
3. Establish credibility
4. Encourage contact

Avoid generic biography-style content. Every section should communicate measurable outcomes, decision making, or technical capability.

# Page Specifications

## Home

Purpose:
Create an immediate, premium first impression.

Sections:
1. Hero
2. About
3. Skills
4. Experience
5. Certifications
6. Featured Projects
7. Contact
8. Footer

## Project Case Study

Each case study page contains:

- Hero banner
- Executive overview
- Business problem
- Objectives
- Solution approach
- Technology stack
- Screenshots / media
- Results & business impact
- GitHub repository
- Live demo

Designed so future deployments can link externally without changing the information architecture.

# UX Principles

- Clean, airy layout
- Maximum readability
- Generous whitespace
- Consistent spacing (8px scale)
- Minimal visual noise
- One primary action per section
- Responsive by design
- Subtle motion only
- Light theme only


# Design System

## Design Philosophy

The visual language should combine:
- 60% Apple-inspired minimalism
- 30% Modern SaaS aesthetics
- 10% Corporate professionalism

Keywords:
Clean • Airy • Elegant • Structured • Calm • Premium

## Color Palette

Primary: #2563EB
Accent: #7C3AED
Background: #F8FAFC
Surface: #FFFFFF
Primary Text: #111827
Secondary Text: #4B5563
Border: #E5E7EB
Success: #16A34A
Warning: #D97706
Error: #DC2626

Gradients should be used sparingly for hero highlights and primary CTAs only.

## Typography

Headings: Poppins
Body: Inter

Scale:
- Display: 56px
- H1: 48px
- H2: 36px
- H3: 28px
- H4: 22px
- Body: 16px
- Small: 14px

## Spacing System

Base unit: 8px

Scale:
4, 8, 16, 24, 32, 48, 64, 80, 96, 128

## Border Radius

Small: 8px
Medium: 12px
Large: 20px
XL: 28px

## Shadows

Level 1: subtle cards
Level 2: hover state
Level 3: modal / elevated surface

Avoid heavy shadows.

## Buttons

Primary:
Filled blue with white text.

Secondary:
White background, subtle border.

Ghost:
Text only for tertiary actions.

## Cards

Project cards:
- Large rounded corners
- Clean image
- Minimal metadata
- Technology chips
- Hover elevation
- No clutter

## Motion

Use Framer Motion.

Animation principles:
- Fade + slight upward motion
- 200–350ms duration
- Ease-out timing
- Respect reduced-motion preferences

Avoid parallax, typing animations, and decorative floating elements.

## Responsive Breakpoints

Mobile: <640px
Tablet: 640–1023px
Desktop: 1024–1439px
Large Desktop: 1440px+

# Component Specifications

Every UI component must be reusable, typed, accessible, and isolated.

Components:
- Header
- Hero
- About
- SkillsGrid
- ExperienceTimeline
- Certifications
- FeaturedProjects
- ProjectCard
- ContactForm
- Footer

No business content should be hardcoded inside components. Components consume structured data objects.


# Technical Architecture

## Technology Stack

Frontend:
- React 19
- TypeScript
- Vite
- Tailwind CSS

UI & Motion:
- Framer Motion
- Lucide React
- React Icons

Integrations:
- EmailJS (contact form)
- Google Analytics 4
- Vercel Analytics

Hosting:
- Vercel

Version Control:
- Git + GitHub

## Folder Structure

```
src/
  assets/
  components/
  data/
  hooks/
  layouts/
  pages/
  routes/
  styles/
  types/
  utils/
  App.tsx
```

## Routing Strategy

Routes:
- /
- /projects/:slug
- /resume

The routing layer must support future additions (blog, chatbot, CMS) without restructuring.

## Data Strategy

All portfolio content shall live in typed data files.

Examples:
- profile.ts
- skills.ts
- experience.ts
- certifications.ts
- projects.ts
- seo.ts

Components must render from data rather than embedding content.

## State Management

Global state should be minimized.

Use:
- React state
- Context only when shared state becomes necessary

Avoid introducing Redux or other heavy state libraries for V1.

## Performance Strategy

- Route-based code splitting
- Lazy-load images
- Optimized fonts
- Tree-shaking
- Minimize bundle size
- Prefer SVG icons
- Cache static assets

## SEO Implementation

Every route should define:
- Title
- Meta description
- Canonical URL
- Open Graph tags
- Twitter card metadata
- Structured JSON-LD where appropriate

## Future Extensibility

Architecture must support:
- Blog
- AI chatbot
- External project deployments
- CMS-backed content
- Additional portfolio sections

No architectural decisions in V1 should block these future enhancements.


# Detailed Component Specifications

## Header

Purpose:
Provide persistent navigation and quick access to the Resume.

Requirements:
- Sticky positioning
- Transparent at page top
- Subtle blur after scrolling
- Active navigation indicator
- Mobile hamburger menu
- Resume CTA aligned right
- Logo scrolls to Hero

Acceptance Criteria:
- Accessible via keyboard
- Responsive on all breakpoints
- No layout shift during scroll

---

## Hero

Purpose:
Communicate value proposition within 10 seconds.

Content:
- Greeting
- Professional headline
- Short positioning statement
- Primary CTA (View Projects)
- Secondary CTA (Resume)
- Minimal background accent

Do NOT include:
- Profile photograph
- Typing animations
- Social counters

Acceptance Criteria:
- Entire Hero visible without excessive scrolling
- Primary CTA immediately visible

---

## About

Purpose:
Explain professional story through business impact.

Requirements:
- Narrative format
- 2–3 concise paragraphs
- Focus on solving business problems
- Avoid chronological resume repetition

---

## Skills

Display grouped skill cards.

Categories:
- Programming
- Analytics
- AI
- Development

Each card includes:
- Icon
- Skill name
- Proficiency (Beginner / Intermediate / Advanced / Expert)

Avoid percentage bars.

---

## Experience Timeline

Vertical timeline.

Each experience entry contains:
- Duration
- Role
- Company (anonymized)
- Key achievements
- Technologies used

---

## Certifications

Grid layout.

Each certification contains:
- Title
- Issuing organization
- Completion year
- Credential link (future)

Placeholder data allowed in MVP.

---

## Featured Projects

Layout:
Responsive card grid.

Card Content:
- Cover image
- Title
- One-line summary
- Technology chips
- Read Case Study button

Optional:
GitHub
Live Demo

No lengthy descriptions on cards.

---

## Contact

Fields:
- Name
- Email
- Message

Validation:
- Client-side validation
- Success state
- Error state

Submission:
EmailJS integration.

---

## Footer

Contains:
- Copyright
- LinkedIn
- GitHub
- Email
- Back to top

# Error, Loading & Empty States

Every asynchronous interaction must define:
- Loading state
- Success state
- Error state
- Empty state

Skeleton loaders preferred over spinners where practical.

# Analytics Strategy

Track:
- Resume downloads
- Project clicks
- Case study visits
- Contact submissions
- External GitHub clicks

Google Analytics and Vercel Analytics should be configurable.



# TypeScript Data Model (Conceptual)

## Profile
- name
- title
- tagline
- summary
- location
- email
- linkedin
- github
- resumeUrl

## Skill
- id
- category
- name
- proficiency

## Experience
- id
- company
- role
- duration
- summary
- achievements[]
- technologies[]

## Project
- id
- slug
- title
- category
- shortDescription
- overview
- businessProblem
- objectives[]
- solution
- techStack[]
- coverImage
- screenshots[]
- githubUrl
- demoUrl
- results[]
- featured

## Certification
- id
- title
- issuer
- year
- credentialUrl

# Acceptance Criteria

## Navigation
- Sticky on all pages
- Accessible via keyboard
- Mobile menu functional

## Projects
- Every card links to a case study
- Tech stack visible
- Images optimized
- Layout responsive

## Contact
- Validation errors are clear
- Successful submission confirmed
- Spam prevention considered

## Overall
- No console errors
- TypeScript strict mode passes
- Responsive across major breakpoints
- Meets defined Lighthouse targets

# Product Roadmap

## Version 1 (MVP)
- Portfolio
- Case studies
- Contact form
- Resume
- SEO
- Analytics
- Responsive UI

## Version 2
- Blog
- Search
- Rich filtering
- Enhanced analytics
- Additional project templates

## Version 3
- AI chatbot
- CMS integration
- Personalized recommendations
- Content management workflow

# Appendix A – Cursor Build Plan

Recommended implementation order:
1. Initialize Vite + React + TS
2. Configure Tailwind
3. Install dependencies
4. Create folder structure
5. Add design tokens
6. Build layout shell
7. Build Header
8. Build Hero
9. Build About
10. Build Skills
11. Build Experience
12. Build Certifications
13. Build Projects grid
14. Build Project card
15. Configure routing
16. Build Case Study template
17. Add Contact form
18. Integrate EmailJS
19. Add SEO
20. Add animations
21. Optimize responsiveness
22. Accessibility audit
23. Performance optimization
24. Analytics integration
25. Final QA
26. Deploy to Vercel

# Appendix B – Core Design Tokens

Spacing: 4,8,16,24,32,48,64,80,96,128
Radius: 8,12,20,28
Motion: 200–350ms ease-out
Grid: 12-column desktop, 8 tablet, 4 mobile

# Appendix C – Coding Standards

- TypeScript strict mode
- Functional React components
- Reusable components only
- No duplicated UI
- Content separated from presentation
- Semantic HTML
- Accessible interactions
- Consistent naming conventions
- Document all reusable utilities

# End of Draft PRD

This document serves as the primary source of truth for implementation. Architecture, design system and implementation documents should derive from this specification to maintain consistency.
