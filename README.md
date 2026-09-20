# GitHub Docs

Welcome to GitHub Docs! GitHub’s documentation is open source, meaning anyone from inside or outside the company can contribute. For full contributing guidelines, visit the official [contributing guide](https://docs.github.com/en/contributing).

> **Note**: This is a public fork of the official [github/docs](https://github.com/github/docs) repository.

---

## Architecture & Directory Structure

| Path | Description |
| :--- | :--- |
| `content/` | Markdown (`.md`) documentation files served on `docs.github.com` |
| `data/` | Reusable text snippets, UI strings, variables, and feature flags |
| `src/` | Next.js application source code, components, middleware, and rendering engine |
| `script/` | Utility scripts for content validation, translation sync, and build checks |
| `.github/` | GitHub Actions workflows, issue templates, and automated review bots |

---

## Quick Start

### Prerequisites
- **Node.js**: `≥ 20.x`
- **npm**: `≥ 10.x`
- **Git**

### Local Setup & Development

1. **Clone your fork:**
   ```bash
   git clone [https://github.com/AnticipatedD/docs.git](https://github.com/AnticipatedD/docs.git)
   cd docs

# Install dependencies:
```bash
npm ci
```
# Start the local development server:
```bash
npm run dev
```
Open http://localhost:4000 in your browser to view the local site.

# Testing & Quality Checks
​Run the following checks before opening a pull request to ensure builds and content validation pass:
```bash
# Run unit and integration tests
npm test

# Run linter checks
npm run lint

# Run content schema and link validation
npm run check-content
```

# Contributing Guidelines

**​Contributor Types**
- **​Open Source Contributors**: Review the Public Contributing Guide for contribution scope and guidelines.
- **​Hubbers (GitHub Employees)**: See `CONTRIBUTING.md` in the `docs-content` or `docs-internal` repositories for internal syncing processes.

# ​Repository Syncing & Scope
​The public `github/docs` repository accepts external contributions strictly for content files (`.md` files in `content/` and select data in `data/` such as reusables).

*​Infrastructure files, site code, and automated workflows are synchronized internally and are closed to external pull requests.*

# ​New to Open Source?
- ​Finding ways to contribute to open source on GitHub
- ​Set up Git
- GitHub flow
- ​Collaborating with pull requests

# ​License
​This project is dual-licensed:
- ​Documentation & Content (`content/`, `data/`, `assets/`): Creative Commons Attribution 4.0 International
- ​Codebase & Scripts: MIT [License](license.md)
