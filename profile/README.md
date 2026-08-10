## Git & Collaboration Workflow
To keep our production firmware stable, safe, and clean, we utilize a secure Forking Workflow. Members hold Read-only access to the main organization repositories and complete all active development through personal forks.

### 1. Fork
Before starting any development, you must create a personal copy of the repository and link it back to the organization:
1. Navigate to the organization repository on GitHub and click the **Fork** button (top right).
2. Select your **personal GitHub account** as the destination.
3. Clone your new personal fork to your local machine using your terminal or GitHub Desktop. (Find Fork HTTPS URL by going to your forked repo and clicking the green code button)

   ```bash
   git clone [Fork HTTPS URL]
   ```

5. Open your terminal inside the project folder (cd REPO PATH) and link it back to the organization source (Find organization HTTPS URL by going to the organization's repo and clicking the green code button):

   ```bash
   git remote add upstream [Organization HTTPS URL]
   ```
   
6. Verify your links by running `git remote -v`. You should see `origin` pointing to your personal account, and `upstream` pointing to the organization.

### 2. Work on a Feature Branch
Always synchronize your local machine with the organization's latest code and create a feature branch before starting a new task:

```bash
git checkout main
git pull upstream main
git checkout -b [feature-branch-name]
```

Now you can freely work on your local machine on the feature branch.

### 3. Commit and Push
Keep your commits descriptive and push your feature branch directly to your personal fork

```bash
git add [file name] OR git add . (to stage all files)
git commit -m "commit message"
git push origin [feature-branch-name]
```

Now your local machine code should be on your forked repo.

We will also use the **Conventional Commits** standard to maintain clean tracking histories. When committing updates via GitHub Desktop, prefix your summaries using the lowercase tokens below:
*   `feat: ` - New features or code implementations
*   `fix: ` - Critical software bug patches or crash resolutions
*   `docs: ` - Edits to markdown documents, charts, or structural code comments
*   `refactor: ` - Optimizing clean execution architectures without changing base logic
*   `chore: ` - Routine maintenance tasks, updating configurations, etc.
*   `test: ` - Modifying mock data endpoints or adding local unit test values

### 4. Open a Pull Request
When your code is complete, working, and ready to be merged into the main project:
1. Go to your forked repo.
2. Go to your feature branch.
3. Click contribute then open pull request.
4. Set the base repository to the organization repo's `main` branch, and set the head repo to your personal fork's feature branch.
5. Fill out the PR template explaining what you built
6. Request a review from one of our **Leads**.

### 5. Review & Merge
* A Lead will review your code changes, provide feedback if needed, and merge it into `main`.
* Once merged, clean up your local machine and synchronize your personal fork:

  ```bash
  git checkout main
  git pull upstream main
  git push origin main
  git branch -d your-feature-branch-name
  git push origin --delete your-feature-branch-name
  ```
  
### 6. Questions
If you have questions or uncertainties regarding set up, workflow, or anything else, feel free to reach out to any of our leads!
