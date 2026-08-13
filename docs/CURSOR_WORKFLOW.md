# CURSOR_WORKFLOW.md

# Cursor Workflow Guide
Version: 1.0

## Purpose
This guide explains how to work with Cursor effectively throughout the project.

## Core Rule
Never ask Cursor to build large features in one prompt. Work incrementally.

## Recommended Session Flow
1. Read the relevant docs (`PRD.md`, `ARCHITECTURE.md`, `DESIGN_SYSTEM.md`, `CURSOR_RULES.md`).
2. Pick one task from `IMPLEMENTATION_PLAN.md`.
3. Ask Cursor to implement only that task.
4. Review all proposed changes before accepting.
5. Test locally.
6. Commit to Git.

## Prompt Template

```text
Read:
- docs/PRD.md
- docs/ARCHITECTURE.md
- docs/DESIGN_SYSTEM.md
- docs/CURSOR_RULES.md

Implement ONLY: <task>

Requirements:
- Do not modify unrelated files.
- Explain every file changed.
- Stop after completing this task.
```

## Good vs Bad Prompts

Bad:
- Build my portfolio.
- Make it look better.
- Fix everything.

Good:
- Build only the Hero section using profile.ts.
- Implement only the Contact form with EmailJS placeholders.
- Refactor ProjectCard into a reusable component.

## When to Ask Cursor to Stop
Always stop after:
- Project setup
- Shared components
- Each homepage section
- Project routing
- Contact form
- Polish

## Reviewing AI Output
Check:
- Architecture consistency
- TypeScript errors
- Hardcoded content
- Accessibility
- Responsive behavior
- Reusable components

Reject changes that:
- Add unnecessary libraries
- Duplicate code
- Ignore design tokens
- Modify unrelated files

## Debugging Prompt

```text
Do not rewrite the feature.
Identify the root cause.
Explain the issue.
Propose the smallest possible fix.
Wait for approval before changing code.
```

## Refactoring Prompt

```text
Improve maintainability without changing UI or behavior.
Reduce duplication.
Keep APIs backward compatible.
```

## Before Every Commit
- Project builds successfully
- No console errors
- Responsive
- TypeScript passes
- Changes limited to intended task

## Daily Workflow
Morning:
- Pull latest changes
- Read next milestone

During work:
- One task per prompt
- Test after every change
- Commit frequently

End of day:
- Push to GitHub
- Record progress
- Note next task

## Golden Rules
- Keep prompts small.
- Let documentation drive implementation.
- Prefer clarity over speed.
- Review every AI-generated change.
