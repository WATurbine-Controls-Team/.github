## Git & Collaboration Workflow
To keep our production firmware stable, safe, and clean, we utilize a secure Forking Workflow. Members hold Read-only access to the main organization repositories and complete all active development through personal forks.

### 1. Fork & Setup Tracking
Before starting any development, you must create a personal copy of the repository and link it back to the organization:
1. Navigate to the organization repository on GitHub and click **Fork** to copy it to your personal profile.
2. Clone your personal fork to your local machine.
3. Open your terminal inside the project directory and configure the organization repository as your upstream remote.
4. Before working on a feature branch, you must pull any updates from `upstream` to keep your local environment up to date and avoid merge conflicts.

### 2. Work on a Feature Branch
Always create a new branch for the specific feature or fix you are working on

### 3. Commit and Push
Keep your commits descriptive and push your feature branch directly to your personal fork

We will also use the **Conventional Commits** standard to maintain clean tracking histories. When committing updates via GitHub Desktop, prefix your summaries using the lowercase tokens below:
*   `feat: ` - New features or code implementations
*   `fix: ` - Critical software bug patches or crash resolutions
*   `docs: ` - Edits to markdown documents, charts, or structural code comments
*   `refactor: ` - Optimizing clean execution architectures without changing base logic
*   `chore: ` - Routine maintenance tasks, updating configurations, etc.
*   `test: ` - Modifying mock data endpoints or adding local unit test values

### 3. Open a Pull Request
When your code is complete, working, and ready to be merged into the main project:
1. Go to the organization repository on GitHub.
2. Click **New Pull Request**
3. Set the base repository to the repository's `main` branch, and set the head repository to your personal fork's feature branch.
4. Fill out the PR template explaining what you built
5. Request a review from one of our **Leads**.

### 4. Review & Merge
A Lead will review your code, provide constructive feedback if needed, and merge it into `main`.

### 5. Questions
If you have questions or uncertainties regarding set up, process, or anything else, feel free to reach out to any of our leads!
