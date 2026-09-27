# CLAUDE.md - Project Context and Agent Guidelines

## Project Overview
Gold Tracker is a client-side mobile-first web application designed for Gold (XAUUSD) traders. It replaces traditional spreadsheets with dynamic capital tracking, 5-day market week logging, projection modeling, and a trading journal. It is deployable to GitHub Pages.

## Build and Run Commands
- Local Preview: `python -m http.server 8000` or `npx -y serve . -l 3000`
- Deployment: Push `main` branch to GitHub and activate GitHub Pages (Root path).

## Engineering Standards & Code Style
- Architecture: Single-Page Application (SPA) using Semantic HTML5, CSS3 Custom Properties, and ES6+ JavaScript modules.
- Storage: LocalStorage with schema validation and export/import fallback.
- Design: Dark mode financial cockpit, glassmorphic styling, high-contrast numerical metrics, responsive mobile viewport.
- CTO Blocking Directives:
  - Zero emoji ban across all files, code comments, and interfaces.
  - Strict input validation on all numerical entries (PnL, targets, capital).
  - Explicit error handling for all LocalStorage access operations.
  - No remote server tracking; all data stays on user device.
  - AI/ directory is strictly local and listed in .gitignore.
