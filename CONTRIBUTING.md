# 🤝 Contributing Guidelines

Thanks for your interest in contributing to this project! To keep things smooth, organized, and stress-free, please follow the steps below when working on new features, bug fixes, or improvements.

---

## 🧱 Branching Strategy

- Always branch off of `main`.
- Use a clear and descriptive naming convention for your branches:
  - `feature/your-feature-name`
  - `bugfix/fix-what-it-does`
  - `hotfix/urgent-fix-name`
  - `chore/cleanup-or-setup-task`

---

## 🚀 Development Workflow

1.  **Pull the latest changes from `main`**
    Before starting any work, make sure your `main` branch is up-to-date.
    ```bash
    git checkout main
    git pull origin main
    ```

2.  **Create a new branch**
    Create a new branch from `main` using the naming convention above.
    ```bash
    git checkout -b feature/your-feature-name
    ```

3.  **Develop and Commit**
    Write your code, test it locally, and commit your changes with clear, descriptive messages.
    - Follow a readable commit style (e.g., [Conventional Commits](https://www.conventionalcommits.org/)):
      - `feat: added login functionality`
      - `fix: correct typo in signup form`
    - Break up large changes into multiple small, logical commits.

4.  **Push your branch**
    Push your new branch to the remote repository.
    ```bash
    git push origin feature/your-feature-name
    ```

5.  **Open a Pull Request (PR)**
    - Go to the repository on GitHub.
    - Click the "Compare & pull request" button for your new branch.
    - Fill out the PR template with a clear description of your changes.
    - Assign reviewers to your PR.
    - Link any related issues by using keywords like `Closes #issue-number` in the PR description.

6.  **Code Review**
    - Wait for your PR to be reviewed. At least one approval is required before merging.
    - Respond to any comments or change requests from the reviewers.
    - If you push new commits to your branch, the approval status may be reset.

7.  **Merge**
    - Once the PR is approved and all checks have passed, the Scrum Master or a project maintainer will merge it into `main`.
    - Squash merges are preferred to maintain a clean and readable commit history.
    - The `main` branch is protected—direct pushes are disabled. All changes must go through a PR.

---

## 📦 Code Quality

-   **Format your code** before pushing to ensure a consistent style across the project.
-   **Write tests** where applicable to cover new features and bug fixes.
-   **Ensure it runs locally** without any errors before opening a pull request.

---

## 💡 Tips

-   Keep your Pull Requests focused and small. As a rule of thumb: one feature or one bug fix per PR.
-   Use **Draft PRs** to signal that your work is in progress and to get early feedback from the team.
-   Never commit sensitive information like `.env` files, credentials, or large binary files.

---
