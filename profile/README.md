## Git & Collaboration Workflow
To keep our production code stable, safe, and clean, we follow a standard branching strategy.

### 1. Work on a Feature Branch
Always create a new branch for the specific feature or fix you are working on

### 2. Commit and Push
Keep your commits descriptive and push your branch to GitHub to back up your progress

We will also use the **Conventional Commits** standard to maintain clean tracking histories. When committing updates via GitHub Desktop, prefix your summaries using the lowercase tokens below:
*   `feat: ` - New features or code implementations (e.g., `feat: add dual-core freertos task for asynchronous api polling`)
*   `fix: ` - Critical software bug patches or crash resolutions (e.g., `fix: resolve task watchdog timeout crash in emergency loop`)
*   `docs: ` - Edits to markdown documents, charts, or structural code comments (e.g., `docs: update pinout mapping table`)
*   `refactor: ` - Optimizing clean execution architectures without changing base logic (e.g., `refactor: move global turbine variables to extern`)
*   `chore: ` - Routine maintenance tasks, updating configurations, or modifying `.gitignore` (e.g., `chore: add arduino compilation artifacts to gitignore`)
*   `test: ` - Modifying mock data endpoints or adding local unit test values (e.g., `test: update endpoint URL to point to local testing server`)

### 3. Open a Pull Request
When your code is complete, working, and ready to be merged into the main project:
1. Go to the repository on GitHub.
2. Click **New Pull Request** from your feature branch into `main`.
3. Fill out the PR template explaining what you built
4. Request a review from one of our **Leads**.

### 4. Review & Merge
A Lead will review your code, provide constructive feedback if needed, and merge it into `main`.
