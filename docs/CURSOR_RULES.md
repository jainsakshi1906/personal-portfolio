# CURSOR_RULES.md

# Cursor AI Coding Rules
Version: 1.0

## Purpose

These rules are mandatory for all AI-generated code in this project. They supplement PRD.md, ARCHITECTURE.md, and DESIGN_SYSTEM.md.

---

# General Principles

- Always follow the PRD before making assumptions.
- Prefer modifying existing code over creating duplicate implementations.
- Ask for clarification rather than inventing functionality when requirements are ambiguous.
- Keep solutions simple, maintainable, and scalable.

---

# Project Architecture

- Never hardcode portfolio content inside React components.
- Read all business content from typed files under `src/data`.
- Keep presentation separate from data.
- Reuse existing layouts and shared components.

---

# React Guidelines

- Use functional components only.
- Use TypeScript strict mode.
- Avoid `any`.
- Keep components focused on a single responsibility.
- Prefer composition over inheritance.

---

# Styling Rules

- Use Tailwind CSS only.
- Follow the 8px spacing scale.
- Use design tokens defined in DESIGN_SYSTEM.md.
- Do not introduce new colors, fonts, or spacing values without approval.
- Avoid inline styles unless absolutely necessary.

---

# UI Guidelines

Do:
- Build reusable components.
- Keep layouts clean and airy.
- Use subtle animations.
- Maintain consistent card and button styles.

Do NOT:
- Add typing animations.
- Add floating particles.
- Add excessive gradients.
- Create progress bars for skills.
- Introduce glassmorphism beyond the documented design system.

---

# Accessibility

- Use semantic HTML.
- Ensure keyboard accessibility.
- Provide alt text for images.
- Maintain visible focus states.
- Preserve proper heading hierarchy.

---

# Performance

- Lazy-load routes and heavy assets.
- Optimize images.
- Prefer SVG icons.
- Avoid unnecessary re-renders.

---

# Dependencies

Do not install new libraries unless:
1. The functionality cannot reasonably be achieved with existing dependencies.
2. The user explicitly approves.

---

# Git Practices

- Make focused, logical commits.
- Avoid unrelated code changes.
- Preserve formatting consistency.

---

# Definition of Done

Every completed task should:
- Compile without errors.
- Pass TypeScript strict mode.
- Match the PRD.
- Respect the Design System.
- Follow the Architecture document.
- Be responsive.
- Be accessible.
- Avoid code duplication.

---

# When Unsure

Cursor should stop and request clarification instead of making assumptions that may conflict with the project documentation.

End of CURSOR_RULES.md
