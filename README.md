# Git Cure

**Terminal-Native Git Diagnostics and Recovery Powered by Gemma 4**

Git Cure is a developer tool designed to diagnose Git repository issues and provide structured, safety-focused recovery recommendations. It combines repository telemetry, AI-assisted diagnosis, recovery planning, and a real-time dashboard to help developers recover from common Git problems.

## Problem Statement

Git errors can be difficult to understand and resolve, especially during hackathons and collaborative development. Issues such as detached HEAD states, merge conflicts, unfinished rebases, and accidental commits to the wrong branch can interrupt development and risk losing uncommitted work.

Developers often rely on online searches and unfamiliar commands to resolve these issues, which can lead to further repository problems.

Git Cure aims to simplify this process by providing clear diagnoses and guided recovery steps directly within the development workflow.

## Proposed Solution

Git Cure acts as a terminal-native Git diagnostic and recovery assistant.

Its key capabilities include:

- **Repository Diagnostics:** Inspects Git repository state and identifies potential issues.
- **AI-Assisted Analysis:** Uses Gemma 4 through OmniRoute to explain detected problems and their possible root causes.
- **Recovery Planning:** Generates structured, step-by-step recovery recommendations.
- **Risk Classification:** Classifies recovery actions according to their potential risk.
- **Safety Snapshots:** Supports creating recovery snapshots before operations that modify repository state.
- **Approval Workflow:** Allows users to review and approve recovery steps where required.
- **Real-Time Dashboard:** Presents repository status, diagnosis results, recovery progress, execution logs, and verification results.

The dashboard serves as a presentation layer. Git operations are handled by the CLI engine rather than executed directly by the frontend.

## System Architecture

The system is organized into the following components:

1. **CLI Engine:** Responsible for repository inspection, Git state detection, and coordinating recovery operations.
2. **Gemma Module:** Analyzes detected issues and produces structured diagnostic results.
3. **Recovery Planner:** Organizes recommended actions into ordered steps and classifies their risks.
4. **Guarded Executor:** Coordinates approved recovery operations, safety snapshots, and verification.
5. **Dashboard:** Displays diagnostics and recovery progress through a React-based interface.

The components communicate through shared TypeScript data contracts and the application's service interfaces.

## Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React, Vite, TypeScript |
| Styling | Tailwind CSS |
| Icons | Lucide |
| Real-Time Communication | Socket.IO |
| CLI Engine | Node.js, TypeScript |
| AI Diagnostics | Gemma 4, OmniRoute |
| Shared Contracts | TypeScript |
| Package Management | npm workspaces |

## Project Structure

```text
Hacktoberfest-Nexora/
├── apps/
│   └── dashboard/       # React dashboard
├── packages/
│   ├── shared/           # Shared TypeScript data contracts
│   └── cli/              # CLI engine
├── services/
│   └── gemma/             # AI diagnosis module
└── docs/                  # Architecture and API documentation
