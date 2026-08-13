# DAY_1_SETUP_GUIDE.md

# Personal Portfolio – Day 1 Setup Guide

## 1. Prerequisites
- GitHub account
- Vercel account
- Cursor Desktop
- Node.js LTS (v20+)
- Git

## 2. Verify Installation
```bash
node -v
npm -v
git --version
```

## 3. Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global init.defaultBranch main
```

## 4. Create Workspace
Recommended:
```
Documents/Projects/personal-portfolio
```

## 5. Create Project
```bash
npm create vite@latest personal-portfolio
cd personal-portfolio
npm install
```
Choose React + TypeScript.

## 6. Open in Cursor
```bash
cursor .
```

## 7. Create docs Folder
Add:
- PRD.md
- ARCHITECTURE.md
- DESIGN_SYSTEM.md
- CURSOR_RULES.md
- IMPLEMENTATION_PLAN.md

## 8. Run Project
```bash
npm run dev
```
Verify the default Vite page loads.

## 9. Connect GitHub
```bash
git init
git remote add origin https://github.com/jainsakshi1906/personal-portfolio.git
```

## 10. First Commit
```bash
git add .
git commit -m "Initial Vite setup"
git branch -M main
git push -u origin main
```

## 11. Before Coding
Read all documentation under `docs/` before asking Cursor to implement anything.

## 12. Daily Workflow
1. Read current milestone.
2. Implement one task.
3. Test locally.
4. Commit.
5. Push.

## 13. Troubleshooting
- Verify Node and Git are installed.
- Re-run `npm install` if dependencies fail.
- Restart the terminal if commands are not recognized.

## 14. End-of-Day Checklist
- No TypeScript errors
- No console errors
- Commit created
- Pushed to GitHub
- Next task identified
