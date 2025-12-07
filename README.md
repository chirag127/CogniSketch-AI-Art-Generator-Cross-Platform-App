<p align="center">
  <img src="https://raw.githubusercontent.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/main/assets/cognisketch-hero.png" alt="CogniSketch Logo" width="250">
</p>

<h1 align="center">CogniSketch-AI-Art-Generator-Mobile-Web-App</h1>

<p align="center">
  <!-- Build Status -->
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/actions/workflows/ci.yml">
    <img src="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/actions/workflows/ci.yml/badge.svg" alt="Build Status" style="max-width: 100%;">
  </a>
  <!-- Code Coverage -->
  <a href="https://codecov.io/gh/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App">
    <img src="https://codecov.io/gh/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/branch/main/graph/badge.svg?token=YOUR_CODECOV_TOKEN" alt="Code Coverage" style="max-width: 100%;">
  </a>
  <!-- Frontend Stack -->
  <img src="https://img.shields.io/badge/Frontend-React_Native-61DAFB?style=flat-square&logo=react" alt="React Native" style="max-width: 100%;">
  <img src="https://img.shields.io/badge/Framework-Expo-000020?style=flat-square&logo=expo" alt="Expo" style="max-width: 100%;">
  <img src="https://img.shields.io/badge/Language-TypeScript-3178C6?style=flat-square&logo=typescript" alt="TypeScript" style="max-width: 100%;">
  <img src="https://img.shields.io/badge/Styling-TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss" alt="TailwindCSS" style="max-width: 100%;">
  <img src="https://img.shields.io/badge/Bundler-Vite-646CFF?style=flat-square&logo=vite" alt="Vite" style="max-width: 100%;">
  <!-- Backend Stack -->
  <img src="https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express" alt="Express.js" style="max-width: 100%;">
  <img src="https://img.shields.io/badge/AI-Google_Gemini-4285F4?style=flat-square&logo=google" alt="Google Gemini" style="max-width: 100%;">
  <!-- Lint/Format -->
  <img src="https://img.shields.io/badge/Linter_Formatter-Biome-60A5FA?style=flat-square&logo=biome" alt="Biome" style="max-width: 100%;">
  <!-- License -->
  <img src="https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey?style=flat-square" alt="License" style="max-width: 100%;">
  <!-- GitHub Stars -->
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App?style=flat-square&color=orange" alt="GitHub Stars" style="max-width: 100%;">
  </a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/stargazers">
    <img src="https://img.com/" alt="Star this Repo" style="width: auto; height: 28px; vertical-align: middle;"> <strong>Star ⭐ this Repo</strong>
  </a>
</p>

--- 

## 🚀 BLUF: Transform Sketches into AI Art

CogniSketch is an innovative cross-platform mobile and web application that empowers users to effortlessly convert their hand-drawn sketches or simple input into stunning, AI-generated artwork across diverse artistic styles. Leveraging React Native for a seamless frontend experience and an Express.js backend integrated with Google Gemini, this full-stack Generative AI showcase brings creative vision to life with unprecedented ease and flexibility.

## 🗺️ Table of Contents

*   [🚀 BLUF: Transform Sketches into AI Art](#-bluf-transform-sketches-into-ai-art)
*   [🗺️ Table of Contents](#️-table-of-contents)
*   [🧠 Architectural Overview](#-architectural-overview)
*   [🤖 AI Agent Directives](#-ai-agent-directives)
*   [📁 Project Structure](#-project-structure)
*   [▶️ Getting Started](#️-getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
    *   [Environment Variables](#environment-variables)
    *   [Running the Application](#running-the-application)
*   [🛠️ Development Scripts](#️-development-scripts)
*   [🧪 Testing](#-testing)
*   [✨ Key Architectural Principles](#-key-architectural-principles)
*   [🤝 Contributing](#-contributing)
*   [🔒 Security](#-security)
*   [📄 License](#-license)
*   [📧 Contact](#-contact)

---

## 🧠 Architectural Overview

CogniSketch employs a modern, decoupled architecture consisting of a React Native-based frontend (serving both mobile and web clients via Expo) and a robust Node.js/Express.js backend. This setup ensures scalability, maintainability, and clear separation of concerns, with AI model interactions handled securely on the server side.

mermaid
graph TD
    A[Mobile/Web Client] -->|HTTP/S Requests| B(Express.js Backend API)
    B -->|API Calls (Gemini)| C(Google Gemini AI Service)
    C -->|Generated Image/Text| B
    B -->|Image Data/Metadata| A

    subgraph Frontend (React Native + Expo)
        A1[User Interface (UI)]
        A2[State Management]
        A3[API Client]
        A[Mobile/Web Client] --- A1
        A1 --- A2
        A2 --- A3
    end

    subgraph Backend (Node.js + Express.js)
        B1[API Endpoints]
        B2[AI Integration Service]
        B3[Data / Storage (Optional)]
        B(Express.js Backend API) --- B1
        B1 --- B2
        B2 --- B3
    end

    style A fill:#61DAFB,stroke:#333,stroke-width:2px
    style B fill:#000,stroke:#333,stroke-width:2px,color:#fff
    style C fill:#4285F4,stroke:#333,stroke-width:2px,color:#fff


---

## 🤖 AI Agent Directives

<details>
<summary>Click to view the Apex Technical Authority Directives</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**. This repository, `CogniSketch-AI-Art-Generator-Mobile-Web-App`, is a **TypeScript-based Full-Stack Mobile/Web Application** with a Node.js backend leveraging Google Gemini.

*   **PRIMARY SCENARIO A: WEB / APP / GUI (Modern Frontend & Backend)**
    *   **Frontend Stack (Mobile/Web):** This project leverages **TypeScript (Strict mode)** for robust type safety across the frontend.
        *   **Framework:** **React Native** with **Expo** for cross-platform mobile and web deployment.
        *   **Build Tool:** **Vite** is used for lightning-fast development and optimized builds.
        *   **Styling:** **TailwindCSS v4** (via NativeWind for React Native) ensures utility-first, highly customizable, and responsive UI.
        *   **Architecture:** Adheres to **Feature-Sliced Design (FSD)** for a scalable and maintainable project structure, organizing code by feature, layer, and slice.
    *   **Backend Stack (API/Logic):**
        *   **Runtime:** **Node.js** with **Express.js** as the web framework.
        *   **AI Integration:** Deeply integrated with **Google Gemini API** (`gemini-3-pro` by default) for image generation from text prompts. Prioritize modular design, clear API contracts, and robust error handling for all AI model interactions.
        *   **Database:** (Implicit or optional, assume lightweight for initial MVP, e.g., local storage or simple file system for user data/preferences, or a NoSQL like MongoDB for scalability if expanded).
        *   **Architecture:** Follows **Hexagonal Architecture (Ports & Adapters)** principles for the backend, ensuring domain logic is decoupled from external dependencies (databases, AI APIs, HTTP frameworks).

*   **LINTING & TESTING STRATEGY:**
    *   **Linting/Formatting:** **Biome** is the unified linter and formatter for both frontend and backend TypeScript/JavaScript code, ensuring consistent code style and catching errors early.
    *   **Frontend Testing:**
        *   **Unit/Component Tests:** **Vitest** (or Jest if specific React Native features require it) for fast unit and component testing.
        *   **End-to-End (E2E) Tests:** **Playwright** for robust cross-browser and cross-platform E2E testing, simulating user interactions in a real browser/device environment.
    *   **Backend Testing:**
        *   **Unit Tests:** **Mocha** and **Chai** for unit testing API logic and utility functions.
        *   **Integration Tests:** Supertest for testing HTTP endpoints and API interactions.

---

## 4. ARCHITECTURAL PATTERNS & PRINCIPLES
*   **SOLID Principles:** Strictly applied (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) to ensure modular, testable, and maintainable code.
*   **DRY (Don't Repeat Yourself):** Promote reusable components, functions, and abstractions.
*   **YAGNI (You Ain't Gonna Need It):** Focus on current requirements, avoid premature optimization or over-engineering.
*   **Modular Design:** Emphasize small, focused modules with clear responsibilities and explicit interfaces.
*   **API-First Approach:** Design APIs with clear contracts and documentation before implementation.
*   **Security by Design:** Implement security best practices from the outset (e.g., input validation, authentication, authorization, secure configuration).
*   **Observability:** Integrate logging, metrics, and tracing for better monitoring and debugging.

---

## 5. REPOSITORY STRUCTURE & DEVELOPMENT WORKFLOW
*   **Version Control:** GitFlow or GitHub Flow for branching strategy.
*   **CI/CD:** GitHub Actions for automated testing, linting, and deployment.
*   **Documentation:** Comprehensive `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, and API documentation.
*   **Dependency Management:** `pnpm` (or `yarn` if preferred by specific React Native tooling) for efficient package management.
*   **Code Review:** Mandatory for all pull requests.
*   **Semantic Versioning:** Follow `MAJOR.MINOR.PATCH` for releases.

---

## 6. VERIFICATION & EXECUTION COMMANDS
*   **Install Dependencies:** `pnpm install`
*   **Run Frontend Dev Server:** `pnpm dev:frontend`
*   **Run Backend Dev Server:** `pnpm dev:backend`
*   **Run All Tests:** `pnpm test`
*   **Run Lint & Format Check:** `pnpm lint`
*   **Run Lint & Format Fix:** `pnpm format:fix`
*   **Build Frontend (Web):** `pnpm build:frontend`
*   **Build Backend:** `pnpm build:backend`
*   **Generate Static Documentation:** (If applicable)

**FAILURE CONDITIONS:** Any deviation from these directives, or failure to meet the outlined standards, will result in immediate termination of the current task and reassignment.
</details>

---

## 📁 Project Structure


.github/
├── workflows/
│   └── ci.yml
├── CONTRIBUTING.md
├── ISSUE_TEMPLATE/
│   └── bug_report.md
├── PULL_REQUEST_TEMPLATE.md
└── SECURITY.md
backend/
├── src/
│   ├── api/
│   ├── config/
│   ├── services/
│   ├── utils/
│   └── app.ts
├── tests/
├── .env.example
├── package.json
└── tsconfig.json
frontend/
├── assets/
├── src/
│   ├── app/
│   ├── entities/
│   ├── features/
│   ├── pages/
│   ├── shared/
│   └── widgets/
├── components/
├── screens/
├── navigation/
├── .env.example
├── App.tsx
├── app.json
├── package.json
└── tsconfig.json
.gitignore
LICENSE
README.md
PROPOSED_README.md
badges.yml
AGENTS.md
package.json  # Monorepo root package.json for pnpm workspace
pnpm-lock.yaml
pnpm-workspace.yaml


---

## ▶️ Getting Started

Follow these steps to set up and run CogniSketch locally.

### Prerequisites

Ensure you have the following installed:

*   [Node.js](https://nodejs.org/en/) (v18.x or later)
*   [pnpm](https://pnpm.io/installation) (for efficient monorepo dependency management)
*   [Expo CLI](https://docs.expo.dev/get-started/installation/) (`npm install -g expo-cli`)
*   A Google Cloud project with the [Gemini API](https://ai.google.dev/) enabled.

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App.git
    cd CogniSketch-AI-Art-Generator-Mobile-Web-App
    

2.  **Install pnpm dependencies for the monorepo:**
    bash
    pnpm install
    

### Environment Variables

Both `backend` and `frontend` directories require their own `.env` files based on their respective `.env.example` templates.

**For `backend/.env`:**

env
PORT=3000
GOOGLE_GEMINI_API_KEY="YOUR_GOOGLE_GEMINI_API_KEY"


**For `frontend/.env`:**

env
EXPO_PUBLIC_API_URL="http://localhost:3000" # Or your deployed backend URL


### Running the Application

Open two separate terminal windows for the frontend and backend.

1.  **Start the Backend API:**
    Navigate to the `backend` directory and start the server.
    bash
    cd backend
    pnpm dev
    
    The backend server will typically run on `http://localhost:3000` (or your specified PORT).

2.  **Start the Frontend (Mobile/Web):**
    Navigate to the `frontend` directory and start the Expo development server.
    bash
    cd frontend
    pnpm start
    
    This will open the Expo Dev Tools in your browser. You can then:
    *   Scan the QR code with your mobile device using the Expo Go app.
    *   Run on an Android emulator or iOS simulator.
    *   Press `w` to run the web application in your browser.

---

## 🛠️ Development Scripts

These scripts are defined in the root `package.json` and in the individual `frontend/package.json` and `backend/package.json` files. Use `pnpm` to execute them from the respective project root.

| Script              | Description                                        | Location   |
| :------------------ | :------------------------------------------------- | :--------- |
| `pnpm install`      | Installs all project dependencies.                 | Root, Frontend, Backend |
| `pnpm dev:frontend` | Starts the frontend development server.            | Root       |
| `pnpm dev:backend`  | Starts the backend development server.             | Root       |
| `pnpm start`        | (Frontend only) Starts Expo dev server.            | Frontend   |
| `pnpm build:frontend` | Builds the frontend for web deployment.            | Frontend   |
| `pnpm test`         | Runs all tests (frontend/backend).                 | Root, Frontend, Backend |
| `pnpm lint`         | Runs Biome linter checks.                          | Root, Frontend, Backend |
| `pnpm format:fix`   | Fixes formatting issues using Biome.               | Root, Frontend, Backend |
| `pnpm typecheck`    | Runs TypeScript type checking.                     | Root, Frontend, Backend |

---

## 🧪 Testing

CogniSketch employs a comprehensive testing strategy:

*   **Unit Tests:**
    *   **Frontend:** `Vitest` for React Native components and utility functions.
    *   **Backend:** `Mocha` and `Chai` for API services and logic.
*   **Integration Tests:** `Supertest` for backend API endpoint validation.
*   **End-to-End (E2E) Tests:** `Playwright` for simulating user flows across mobile/web clients and backend interactions.

To run all tests from the root of the repository:

bash
pnpm test


---

## ✨ Key Architectural Principles

*   **Feature-Sliced Design (FSD):** Applied to the frontend for clear separation of concerns, ensuring scalability and maintainability.
*   **Hexagonal Architecture (Ports & Adapters):** Employed in the backend to decouple business logic from external dependencies.
*   **SOLID Principles:** Enforced throughout the codebase to promote modular, testable, and robust code.
*   **API-First Design:** Backend API is designed with clear contracts and robust error handling.
*   **Type Safety:** Extensive use of TypeScript with strict configurations to minimize runtime errors and improve developer experience.

---

## 🤝 Contributing

We welcome contributions to CogniSketch! Please refer to our [CONTRIBUTING.md](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/.github/CONTRIBUTING.md) for guidelines on how to submit issues, pull requests, and set up your development environment.

---

## 🔒 Security

Security is a top priority. Please review our [SECURITY.md](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/.github/SECURITY.md) to learn how to report vulnerabilities and our security practices.

---

## 📄 License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) License](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/LICENSE).

---

## 📧 Contact

For any questions or inquiries, please reach out to [chirag127](https://github.com/chirag127).
