# SpecKit Agent Starter Kit

This is a reusable starter kit for setting up a **Multi-Agent, Spec-Driven Development** workflow in any project.

## 📦 Contents

- **`.github/agents/`**: Contains the 3 Core Agents (Project Lead, PM Lead, Engineering Lead).
- **`.speckit/`**: Contains the Global Constitution.
- **`ARCHITECTURE.md`**: A template for your project's technical stack.

## 🚀 How to Use

1.  **Copy Files:** Copy the `.github`, `.speckit`, and `ARCHITECTURE.md` folders/files to the root of your new project repository.
2.  **Initialize Architecture:** Open `ARCHITECTURE.md` and fill in your specific Tech Stack (Language, Frameworks, etc.).
3.  **Configure VS Code:** Ensure you have an AI extension (like GitHub Copilot Chat) that can see these agent definitions.
4.  **Start:** Open a chat with the **Project Lead Agent** and say: *"I want to start a new feature called [Name]."*

## 🛠️ Prerequisites

- **VS Code**
- **GitHub CLI (`gh`)**: Must be installed and authenticated (`gh auth login`).
- **Git**: Initialized repository.

## 🔄 Workflow Overview

1.  **Project Lead** creates a Tracking Issue on GitHub.
2.  **PM Lead** writes Specs -> Commits -> Opens PR.
3.  **You** review and merge the Spec PR.
4.  **Engineering Lead** plans tasks -> Creates GitHub Issues.
5.  **Engineering Lead** writes code -> Opens PRs.
6.  **You** review and merge Code PRs.
