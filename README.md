# Git Cure

**Terminal-native Git diagnostics and recovery powered by Gemma 4.**

Git Cure helps developers identify Git repository issues, understand their root causes, and follow a structured recovery plan.

## Problem

Developers frequently encounter Git issues such as detached HEAD states, merge conflicts, unfinished rebases, and accidental commits to the wrong branch. Recovering from these situations can be confusing and may risk losing uncommitted work.

## Solution

Git Cure acts as a Git Doctor that:

- **Detects:** Inspects repository status and Git history to identify problems.
- **Diagnoses:** Uses Gemma 4 through OmniRoute to explain root causes.
- **Plans:** Generates step-by-step recovery recommendations.
- **Protects:** Uses safety snapshots and approval steps before recovery actions.
- **Visualizes:** Provides a dashboard for repository diagnostics and recovery progress.

## Tech Stack

- **Frontend:** React, Vite, TypeScript, Tailwind CSS
- **Backend:** Node.js, TypeScript
- **AI:** Gemma 4 via OmniRoute
- **Communication:** Socket.IO
- **Package Management:** npm workspaces

## Project Structure

```text
apps/dashboard/   # React dashboard
packages/shared/  # Shared TypeScript types
packages/cli/     # CLI engine
services/gemma/   # Gemma diagnostics
docs/             # Project documentation
