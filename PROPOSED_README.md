<!-- Hero Banner: Replace with your project's logo or a captivating image -->
![CogniSketch Logo](https://raw.githubusercontent.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/main/.github/assets/cognisketch-hero.png)

# CogniSketch-AI-Art-Generator-Mobile-Web-App

<p align="center">
  <!-- Badges -->
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/ci.yml?branch=main&style=flat-square&label=Build%20Status" alt="Build Status">
  </a>
  <a href="https://codecov.io/gh/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App">
    <img src="https://img.shields.io/codecov/c/github/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App?style=flat-square&token=YOUR_CODECOV_TOKEN" alt="Code Coverage">
  </a>
  <img src="https://img.shields.io/badge/Language-TypeScript-blue?style=flat-square" alt="Language">
  <img src="https://img.shields.io/badge/Frontend-React%20Native%20%7C%20Expo-61DAFB?style=flat-square&logo=react" alt="Frontend">
  <img src="https://img.shields.io/badge/Backend-Node.js%20%7C%20Express-green?style=flat-square&logo=nodedotjs" alt="Backend">
  <img src="https://img.shields.io/badge/AI%20API-Google%20Gemini-orange?style=flat-square&logo=google" alt="AI API">
  <img src="https://img.shields.io/badge/Linting-Biome-blueviolet?style=flat-square&logo=biome" alt="Linting">
  <img src="https://img.shields.io/badge/Testing-Vitest-brightgreen?style=flat-square&logo=vitest" alt="Testing">
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square" alt="License">
  </a>
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App?style=flat-square&color=yellow" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/stargazers">
    <img src="https://img.shields.io/badge/Star%20⭐%20this%20Repo-Join%20our%20community!-brightgreen?style=social&label=Stars" alt="Star this Repo">
  </a>
</p>

## Project Overview

CogniSketch is an advanced, cross-platform mobile and web application designed to revolutionize artistic creation by transforming user sketches into stunning AI-generated artwork. Leveraging the power of React Native for a seamless frontend experience and an Express.js backend integrated with the Google Gemini API, this full-stack solution offers diverse artistic styles and a robust generative AI showcase.

## Architecture

CogniSketch employs a modern, modular architecture comprising a React Native frontend for mobile and web, an Express.js backend for API orchestration, and deep integration with the Google Gemini API for powerful AI inference. The frontend follows a Feature-Sliced Design, ensuring clear separation of concerns, while the backend adopts a Modular Monolith approach for scalable service management.

mermaid
graph TD
    A[Mobile/Web Frontend <br> (React Native/Expo)] --> B(Express.js Backend)
    B --> C[Google Gemini API <br> (AI Art Generation)]
    C --> B
    B --> A
    subgraph Core Components
        A
        B
        C
    end


## Table of Contents

-   [Project Overview](#project-overview)
-   [Architecture](#architecture)
-   [Table of Contents](#table-of-contents)
-   [Key Features](#key-features)
-   [Getting Started](#getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
    -   [Running the Application](#running-the-application)
-   [Development Standards](#development-standards)
    -   [Scripts](#scripts)
    -   [Architectural Principles](#architectural-principles)
-   [🤖 AI Agent Directives](#ai-agent-directives)
-   [Contributing](#contributing)
-   [License](#license)
-   [Security](#security)

## Key Features

*   **Sketch-to-Art Transformation:** Convert simple user sketches into sophisticated AI-generated images.
*   **Diverse Artistic Styles:** Choose from a wide array of pre-defined and customizable artistic styles.
*   **Cross-Platform Accessibility:** Deployable as a native mobile app (iOS/Android) via Expo and a responsive web application.
*   **Google Gemini Integration:** Harness the latest generative AI capabilities for superior image quality and creative freedom.
*   **Full-Stack Observability:** Comprehensive logging, monitoring, and error handling for both frontend and backend.
*   **High Performance:** Optimized for fast rendering and efficient AI processing.

## Getting Started

Follow these steps to set up and run CogniSketch locally.

### Prerequisites

Ensure you have the following installed:

*   Node.js (LTS version, e.g., v20.x)
*   npm or Yarn
*   Expo CLI (`npm install -g expo-cli`)
*   Access to Google Gemini API with a valid API Key.

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App.git
    cd CogniSketch-AI-Art-Generator-Mobile-Web-App
    

2.  **Install frontend dependencies:**
    bash
    cd frontend
    npm install # or yarn install
    

3.  **Install backend dependencies:**
    bash
    cd ../backend
    npm install # or yarn install
    

4.  **Configure Environment Variables:**
    Create a `.env` file in the `backend` directory and add your Google Gemini API key:
    
    GEMINI_API_KEY=YOUR_GOOGLE_GEMINI_API_KEY
    
    (Optional) For frontend, if direct API calls are made, ensure environment variables are configured via Expo's `app.config.js` or similar for build-time injection.

### Running the Application

1.  **Start the Backend Server:**
    bash
    cd backend
    npm run dev # or yarn dev
    
    The backend server will typically run on `http://localhost:3000`.

2.  **Start the Frontend Application:**
    Open a new terminal, navigate to the `frontend` directory:
    bash
    cd frontend
    npm start # or yarn start
    
    This will open the Expo Developer Tools. You can then choose to:
    *   Scan the QR code with your mobile device using the Expo Go app.
    *   Run on an iOS simulator (press `i`).
    *   Run on an Android emulator (press `a`).
    *   Run in your web browser (press `w`).

## Development Standards

### Scripts

A comprehensive set of scripts is available for development and maintenance:

| Script              | Description                                                                 | Location   |
| :------------------ | :-------------------------------------------------------------------------- | :--------- |
| `npm run start`     | Starts the Expo development server for the frontend.                        | `frontend` |
| `npm run dev`       | Starts the backend server in development mode.                              | `backend`  |
| `npm run build`     | Builds the frontend for production (web/mobile bundles).                    | `frontend` |
| `npm run lint`      | Runs Biome linter and formatter across the project.                         | `root`     |
| `npm run format`    | Formats code using Biome.                                                   | `root`     |
| `npm test`          | Executes all unit and integration tests with Vitest.                        | `root`     |
| `npm run test:e2e`  | Runs end-to-end tests with Playwright (for web) / Detox (for mobile).       | `root`     |
| `npm run typecheck` | Checks TypeScript types across the project.                                 | `root`     |

### Architectural Principles

This project strictly adheres to established architectural principles to ensure maintainability, scalability, and robustness:

*   **Feature-Sliced Design (FSD):** Applied to the frontend for clear and consistent structuring by features, layers, and slices, promoting modularity and reuse.
*   **Modular Monolith:** The backend is organized as a modular monolith, allowing for distinct domain-driven modules while maintaining a unified deployment.
*   **SOLID Principles:** Embraced for object-oriented design (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion).
*   **DRY (Don't Repeat Yourself):** Emphasis on abstracting common logic and components to minimize redundancy.
*   **YAGNI (You Aren't Gonna Need It):** Prioritizing current requirements and avoiding premature optimization or over-engineering.
*   **API-First Design:** All backend services are designed with clear API contracts, promoting loose coupling and independent evolution.

<details>
<summary><h2>🤖 AI Agent Directives</h2></summary>

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
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**. This repository, `CogniSketch-AI-Art-Generator-Mobile-Web-App`, is a cross-platform mobile/web application with a backend.

*   **PRIMARY SCENARIO: WEB / APP / GUI (Modern Frontend & Backend)**
    *   **Frontend Stack:** This project leverages **React Native** (Expo SDK 50+) for cross-platform mobile and web UI. Key tools include **TypeScript** (Strict mode enforced), **Vite** (for web bundling and development), and **TailwindCSS v4** (via NativeWind for React Native compatibility). State management should prefer standard React Context or modern hooks, potentially leveraging Signals for highly reactive components.
    *   **Backend Stack:** Implemented with **Node.js** and **Express.js**, written entirely in **TypeScript**. Focus on RESTful API design, robust error handling, and efficient middleware.
    *   **AI Integration:** Deeply integrated with **Google Gemini API** (`gemini-3-pro` by default) for intelligent sketch-to-art generation. Prioritize modular design, clear API contracts, robust error handling, and secure credential management for all AI model interactions.
    *   **Lint/Test:** **Biome** (for ultra-fast linting and formatting across both frontend and backend), **Vitest** (for robust unit and integration testing of both frontend logic and backend services), and **Playwright** (for E2E testing of the web application). For native mobile E2E, consider **Detox** or Appium if specific native interactions are required.

*   **ARCHITECTURAL PATTERNS:**
    *   **Frontend:** Strictly adheres to **Feature-Sliced Design (FSD)**, organizing code by features, layers (app, processes, pages, widgets, features, entities, shared), and slices. This ensures high modularity, scalability, and ease of understanding.
    *   **Backend:** Adopts a **Modular Monolith** pattern, ensuring clear separation of concerns for distinct domains (e.g., user management, sketch processing, AI integration) while maintaining a unified deployment. Emphasis on clear API boundaries between modules.
    *   **General Principles:** Enforce **SOLID**, **DRY**, and **YAGNI** principles throughout the codebase.

*   **VERIFICATION COMMANDS:**
    *   **Lint & Format:** `npm run lint` (or `biome check . && biome format .`)
    *   **Type Check:** `npm run typecheck` (or `tsc --noEmit`)
    *   **Unit/Integration Tests:** `npm test` (or `vitest run`)
    *   **E2E Tests (Web):** `npm run test:e2e -- --project=chromium` (Playwright)
    *   **E2E Tests (Mobile):** `npm run test:e2e:native` (Detox, if implemented)
    *   **Build Frontend:** `cd frontend && npm run build`
    *   **Build Backend:** `cd backend && npm run build`

</details>

## Contributing

We welcome contributions! Please see our [CONTRIBUTING.md](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/.github/CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the [CC BY-NC 4.0 License](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/LICENSE).

## Security

Please review our [SECURITY.md](https://github.com/chirag127/CogniSketch-AI-Art-Generator-Mobile-Web-App/blob/main/.github/SECURITY.md) for information on reporting vulnerabilities and security practices.
