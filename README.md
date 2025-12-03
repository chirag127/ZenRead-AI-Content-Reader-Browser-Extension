# ZenRead-AI-Reader-And-TTS-Browser-Extension

<!-- Hero Banner/Logo Placeholder: Add your project's distinct visual identity here. -->
<p align="center">
  <img src="https://raw.githubusercontent.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/main/assets/zenread-logo.png" alt="ZenRead Logo" width="200"/>
</p>

<p align="center">
  <!-- Build Status -->
  <a href="https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/ci.yml?branch=main&style=flat-square" alt="Build Status">
  </a>
  <!-- Code Coverage (Placeholder - requires setup) -->
  <a href="https://codecov.io/gh/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension">
    <img src="https://img.shields.io/codecov/c/github/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension?style=flat-square&token=YOUR_CODECOV_TOKEN" alt="Code Coverage">
  </a>
  <!-- Tech Stack: JavaScript, Browser Extension -->
  <img src="https://img.shields.io/badge/Tech-JavaScript%20%7C%20WebExtension%20%7C%20Gemini%20AI-blueviolet?style=flat-square" alt="Tech Stack">
  <!-- Lint/Format: Biome -->
  <img src="https://img.shields.io/badge/Code%20Quality-Biome-brightgreen?style=flat-square" alt="Biome">
  <!-- License -->
  <a href="https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square" alt="License">
  </a>
  <!-- GitHub Stars -->
  <a href="https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension?style=flat-square&colorA=DD2476&colorB=FF69B4&label=Stars" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  Star ⭐ this Repo
</p>

ZenRead is a cutting-edge, privacy-focused browser extension engineered to transform your online reading experience. It integrates AI-powered reader mode, advanced text-to-speech capabilities, and Gemini AI-driven summaries directly within your browser, ensuring no data leaves your device.

## Table of Contents

- [ZenRead-AI-Reader-And-TTS-Browser-Extension](#zenread-ai-reader-and-tts-browser-extension)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Architecture Overview](#architecture-overview)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Development Setup](#development-setup)
  - [Project Structure](#project-structure)
  - [Contributing](#contributing)
  - [License](#license)
  - [Security](#security)
  - [AI Agent Directives: Operational Protocol (ZenRead Edition)](#ai-agent-directives-operational-protocol-zenread-edition)

## Features

*   **AI-Powered Reader Mode:** Cleans up web pages, removing distractions and ads for a focused reading experience.
*   **Advanced Text-to-Speech (TTS):** Converts article content into natural-sounding audio, supporting multiple languages and voices.
*   **Gemini AI Summarization:** Get concise, AI-generated summaries of lengthy articles without sending your data to external servers.
*   **Privacy-First Design:** All processing (reader mode, TTS, summarization) happens locally in your browser; no servers, no tracking, no data collection.
*   **Cross-Browser Compatibility:** Supports Chrome, Firefox, and other Chromium-based browsers.
*   **Customizable Settings:** Personalize fonts, themes, TTS voices, and summarization depth.

## Architecture Overview

ZenRead operates as a robust browser extension, meticulously designed to provide powerful features without compromising user privacy. Its architecture is composed of several key components:

*   **Background Script:** Manages core logic, API interactions (Gemini AI, Text-to-Speech), and communication with other parts of the extension. It acts as the central orchestrator.
*   **Content Scripts:** Injected directly into web pages to manipulate the DOM for reader mode and capture text for TTS/summarization. Operates with isolated worlds for security.
*   **Popup UI:** The user-facing interface that provides quick access to features, settings, and controls.
*   **Options Page:** A dedicated page for more extensive configuration and customization of ZenRead's behavior.
*   **Local Storage:** Utilized for storing user preferences and settings securely on the client-side, reinforcing the privacy-first approach.

## Installation

### For Users (Coming Soon)

ZenRead will soon be available on the Chrome Web Store and Firefox Add-ons. Stay tuned for direct links.

### For Developers

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension.git
    cd ZenRead-AI-Reader-And-TTS-Browser-Extension
    
2.  **Install dependencies:**
    bash
    npm install # or yarn install or pnpm install
    
3.  **Load the extension in your browser:**
    *   **Chrome/Brave/Edge:**
        1.  Navigate to `chrome://extensions`.
        2.  Enable "Developer mode" in the top right.
        3.  Click "Load unpacked" and select the `dist` directory (after running `npm run build`).
    *   **Firefox:**
        1.  Navigate to `about:debugging#/runtime/this-firefox`.
        2.  Click "Load Temporary Add-on..." and select any file within the `dist` directory (after running `npm run build`).

## Usage

1.  **Activate Reader Mode:** Click the ZenRead icon in your browser toolbar on an article page to toggle reader mode.
2.  **Text-to-Speech:** While in reader mode, use the controls in the popup to initiate text-to-speech playback.
3.  **Summarize:** On a supported page, click the ZenRead icon and select the "Summarize" option to get a Gemini AI-powered summary.
4.  **Settings:** Access the options page to customize ZenRead's behavior, including default voices, themes, and summarization preferences.

## Development Setup

ZenRead uses a modern JavaScript toolchain for efficient development.

*   **Technologies:** JavaScript (ES2022+), WXT, Vite 7, TailwindCSS v4, Google Gemini API.
*   **Linting & Formatting:** Biome
*   **Testing:** Vitest (Unit/Integration), Playwright (E2E)

### Available Scripts

| Script              | Description                                                                 |
| :------------------ | :-------------------------------------------------------------------------- |
| `npm run dev`       | Starts the development server with hot-reloading for extension components.  |
| `npm run build`     | Compiles and bundles the extension for production deployment.               |
| `npm run lint`      | Runs Biome linter and formatter to check code quality.                      |
| `npm run lint:fix`  | Runs Biome to automatically fix linting and formatting issues.              |
| `npm run test`      | Executes all unit and integration tests with Vitest.                       |
| `npm run test:e2e`  | Runs end-to-end tests across browsers using Playwright.                     |
| `npm run typecheck` | Checks TypeScript files for type errors (if TypeScript is enabled).         |
| `npm run clean`     | Removes build artifacts and temporary files.                                |

## Project Structure


ZenRead-AI-Reader-And-TTS-Browser-Extension/
├── .github/                       # GitHub workflow configurations, templates
├── public/                        # Static assets for the extension
├── src/                           # Source code for the extension
│   ├── background/                # Background script logic
│   ├── content-scripts/           # Scripts injected into web pages
│   ├── popup/                     # Popup UI and logic
│   ├── options/                   # Options page UI and logic
│   ├── api/                       # Gemini AI and TTS API integrations
│   ├── components/                # Reusable UI components
│   ├── services/                  # Core services (e.g., reader mode, summarizer)
│   └── utils/                     # Utility functions
├── assets/                        # Images, logos, etc. for documentation
├── .gitignore                     # Files/directories to ignore in Git
├── .prettierignore                # Files/directories to ignore in Prettier
├── biome.json                     # Biome configuration
├── package.json                   # Project dependencies and scripts
├── tsconfig.json                  # TypeScript configuration
├── vite.config.ts                 # Vite bundler configuration
├── wxt.config.ts                  # WXT (Web Extension Toolkit) configuration
├── README.md                      # This README file
└── LICENSE                        # Project license


## Contributing

We welcome contributions to ZenRead! Please see our [CONTRIBUTING.md](https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/blob/main/.github/CONTRIBUTING.md) for guidelines on how to get started, including information on setting up your development environment, submitting pull requests, and coding standards.

## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) License. See the [LICENSE](https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/blob/main/LICENSE) file for details.

## Security

Your security is our top priority. For information on reporting vulnerabilities or our security practices, please refer to our [SECURITY.md](https://github.com/chirag127/ZenRead-AI-Reader-And-TTS-Browser-Extension/blob/main/.github/SECURITY.md) file.

<details>
<summary><h2>🤖 AI AGENT DIRECTIVES: OPERATIONAL PROTOCOL (ZENREAD EDITION)</h2></summary>

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
**Directives:** This project is a JavaScript-based Browser Extension.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (JavaScript/TypeScript)**
    *   **Stack:** This project leverages **JavaScript (ES2022+)** for maximum browser compatibility and performance. Key tools include **WXT** (for Web Extension development, build process, and cross-browser compatibility), **Vite 7** (for lightning-fast development server and optimized builds), and **TailwindCSS v4** (for utility-first styling). **TypeScript (Strict mode)** is employed for enhanced type safety and maintainability.
    *   **Lint/Test:** **Biome** (for ultra-fast linting and formatting), **Vitest** (for unit and integration testing of JavaScript modules), and **Playwright** (for robust end-to-end testing of extension functionality across different browsers).
    *   **Architecture:** Adheres to a **Browser Extension Architecture** with clear separation between background scripts, content scripts, popup UIs, and options pages. Emphasizes message passing for secure inter-component communication. Follows **Feature-Sliced Design (FSD)** principles where applicable for complex UI/feature organization, and **SOLID/DRY** principles for core logic.
    *   **AI Integration:** Deeply integrated with **Google Gemini API** (`gemini-3-pro` by default) for intelligent text summarization. Prioritize modular design, clear API contracts, and robust error handling for all AI model interactions, ensuring privacy by keeping processing client-side where possible.
    *   **State Management:** Utilizes modern JavaScript patterns (e.g., Signals, or lightweight reactivity libraries) for efficient state management within the popup and options pages.

*   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go) - *Not applicable for this project's primary function. Reference only for potential future native integrations.***
    *   **Stack:** Rust (Cargo) or Go (Modules).
    *   **Lint:** Clippy / GolangCI-Lint.
    *   **Architecture:** Hexagonal Architecture (Ports & Adapters).

*   **SECONDARY SCENARIO C: DATA / AI / SCRIPTS (Python) - *Not applicable for this project. Reference only for potential future backend services.***
    *   **Stack:** uv (Manager), Ruff (Linter), Pytest (Test).
    *   **Architecture:** Modular Monolith or Microservices.

---

## 4. ARCHITECTURAL PATTERNS & PRINCIPLES
*   **Browser Extension Architecture:**
    *   **Background Script:** Centralized event handling, API calls, message dispatch.
    *   **Content Scripts:** DOM manipulation, direct page interaction. Isolated from the page's JS context.
    *   **Popup/Options Pages:** User interaction, settings management.
    *   **Message Passing:** Strict communication between components using `chrome.runtime.sendMessage` and `chrome.runtime.onMessage` for secure data exchange.
*   **SOLID Principles:**
    *   **Single Responsibility Principle (SRP):** Each module, function, or component should have only one reason to change (e.g., `readerModeProcessor.js`, `ttsService.js`, `geminiSummarizer.js`).
    *   **Open/Closed Principle (OCP):** Software entities should be open for extension but closed for modification (e.g., using configuration objects for new AI models).
    *   **Liskov Substitution Principle (LSP):** Subtypes must be substitutable for their base types without altering the correctness of the program (critical for future AI model or TTS engine swaps).
    *   **Interface Segregation Principle (ISP):** Clients should not be forced to depend on interfaces they do not use (e.g., specific message types for specific functionalities).
    *   **Dependency Inversion Principle (DIP):** Depend on abstractions, not concretions (e.g., defining an `ITextToSpeechService` interface).
*   **DRY (Don't Repeat Yourself):** Avoid redundant code. Abstract common functionalities into reusable modules (e.g., utility functions, shared configuration).
*   **YAGNI (You Ain't Gonna Need It):** Implement only features that are currently required. Avoid over-engineering for speculative future needs.
*   **Test-Driven Development (TDD):** Write tests before writing the code to ensure functionality and robustness.
*   **Atomic Commits:** Each commit should represent a single, complete logical change.

---

## 5. DEVELOPMENT WORKFLOW & VERIFICATION COMMANDS
*   **Verification & Testing:**
    *   **Unit Tests:** `npm run test:unit` (Vitest)
    *   **Integration Tests:** `npm run test:integration` (Vitest)
    *   **End-to-End (E2E) Tests:** `npm run test:e2e` (Playwright against browser environments)
    *   **Linting & Formatting:** `npm run lint` (Biome)
    *   **Type Checking:** `npm run typecheck` (TypeScript)
    *   **Build Extension:** `npm run build` (WXT)

*   **Standard Operating Procedures:**
    1.  **Feature Branching:** Develop all features in dedicated branches (`feat/`, `fix/`, `chore/`).
    2.  **Code Review:** Mandatory peer review before merging to `main`.
    3.  **Automated Checks:** Ensure CI/CD pipelines pass (lint, test, build) before merge.
    4.  **Documentation:** Keep `README.md`, `CONTRIBUTING.md`, and `SECURITY.md` up-to-date.
    5.  **Performance Focus:** Prioritize efficient algorithms and minimal resource usage, especially for browser extensions.
    6.  **Privacy by Design:** Ensure all features adhere to the "no servers, no tracking" principle.

---

## 6. SECURITY PROTOCOL
*   **Content Security Policy (CSP):** Strict CSP defined in `manifest.json`.
*   **Input Validation:** Sanitize all user inputs and messages passed between extension components.
*   **Least Privilege:** Request only necessary permissions in `manifest.json`.
*   **API Key Management:** API keys (e.g., Gemini) must be handled securely, ideally loaded from environment variables during development or securely managed in browser storage for client-side use. Never hardcode.
*   **Dependency Auditing:** Regularly audit dependencies for known vulnerabilities.
*   **Cross-Site Scripting (XSS) Prevention:** Strict DOM sanitization for any content injected into web pages.
</details>