# CogniSketch AI Art Generator – Cross‑Platform App

![CogniSketch Logo](https://raw.githubusercontent.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/main/assets/logo.png)

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/ci.yml?branch=main&style=flat-square)](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/actions)
[![Coverage](https://img.shields.io/codecov/c/github/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App?style=flat-square)](https://codecov.io/gh/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App)
[![Tech Stack](https://img.shields.io/badge/Tech-React%20Native%20|%20Express%20|%20TypeScript%20|%20Cerebras%20AI-61DAFB?style=flat-square)](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App)
[![Lint](https://img.shields.io/badge/Lint-Biome-60B9A1?style=flat-square)](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App)
[![License](https://img.shields.io/badge/License-CC%20BY‑NC%204.0-4285F4?style=flat-square)](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/blob/main/LICENSE)
[![Stars](https://img.shields.io/github/stars/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App?style=flat-square)](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App)

[⭐️ Star this repo](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App)

---

## 📌 TL;DR
Turn sketches, photos, or doodles into stunning AI‑generated artwork (Anime, Watercolor, Oil Paint, etc.) on iOS, Android, and the web—powered by Cerebras inference models with a single tap.

---

## 📚 Table of Contents
- [Architecture Overview](#architecture-overview)
- [Quick Start](#quick-start)
- [Development Scripts](#development-scripts)
- [Design Principles](#design-principles)
- [AI Agent Directives](#ai-agent-directives)
- [Contributing](#contributing)
- [License](#license)

---

## 🏗️ Architecture Overview
text
.
├─ .github/               # CI/CD, issue & PR templates
├─ src/                   # React Native front‑end (feature‑sliced)
│   ├─ app/               # Global providers & navigation
│   ├─ features/          # Domain‑specific feature modules
│   └─ shared/            # UI components, hooks, utils
├─ server/                # Express API gateway
│   ├─ routes/            # REST endpoints for asset handling
│   └─ services/          # Cerebras inference wrapper
├─ tests/                 # Vitest unit & Playwright E2E tests
└─ scripts/               # Build & deployment helpers


**Mermaid diagram**
mermaid
flowchart LR
    subgraph Mobile & Web
        UI[React Native UI]
    end
    subgraph Backend
        API[Express API]
        AI[Cerebras Inference Service]
    end
    UI --> API --> AI


---

## 🚀 Quick Start
bash
# Clone the repository
git clone https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App.git
cd CogniSketch-AI-Art-Generator-Cross-Platform-App

# Install dependencies (uses pnpm for speed)
pnpm install

# Set up environment variables
cp .env.example .env
# Edit .env and add CEREBRAS_API_KEY

# Run the development server (mobile and web)
pnpm run dev   # Starts Expo for mobile & Vite for web


---

## 📜 Development Scripts
| Script | Description |
|--------|-------------|
| `dev` | Starts Expo (iOS/Android) and Vite (web) in watch mode |
| `build` | Produces production bundles for web & mobile |
| `lint` | Runs Biome linting and auto‑fix |
| `test` | Executes Vitest unit tests |
| `e2e` | Runs Playwright end‑to‑end suite |
| `ci` | Composite script used by GitHub Actions |

---

## 🧩 Design Principles
- **SOLID** – Each feature slice respects single‑responsibility and dependency inversion.
- **DRY** – Shared UI primitives live in `src/shared`.
- **YAGNI** – Only the AI styles required for MVP are implemented; additional styles are added via plugins.
- **Hexagonal** – The server treats the Cerebras service as an external port, making it swappable.

---

## 🤖 AI Agent Directives
<details>
<summary>Expand for technical directives used by autonomous agents</summary>

**Tech Stack Definition**
- Frontend: React Native (TypeScript) + Expo + Vite
- Backend: Node.js (TypeScript) + Express
- AI Provider: Cerebras Inference via OpenAI SDK (model cascade as defined in AGENTS.md)
- Linting/Formatting: Biome (strict mode)
- Testing: Vitest (unit) + Playwright (E2E)
- CI/CD: GitHub Actions – `ci.yml`

**Architectural Patterns**
- Feature‑Sliced Design (FSD) for UI modules
- Hexagonal Architecture for server side (Ports & Adapters)
- Repository Pattern for data access
- Command‑Query Separation for service layer

**Verification Commands**
bash
# Lint & format check
pnpm run lint

# Unit tests with coverage
pnpm run test --coverage

# End‑to‑end tests (requires emulator or browser)
pnpm run e2e

# Full CI pipeline (local simulation)
pnpm run ci


**Operational Guidelines**
- Respect `MAX_WORKERS=5` when invoking Cerebras inference.
- Apply exponential back‑off on HTTP 429/500 as per Base Agents MD.
- Environment variable `CEREBRAS_API_KEY` must be present in all CI runs.

</details>

---

## 🤝 Contributing
Please read [CONTRIBUTING.md](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/blob/main/CONTRIBUTING.md) for guidelines on how to submit bugs, feature requests, and pull requests.

---

## 📄 License
This project is licensed under the **Creative Commons Attribution‑NonCommercial 4.0 International** License – see the [LICENSE](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Cross-Platform-App/blob/main/LICENSE) file for details.
