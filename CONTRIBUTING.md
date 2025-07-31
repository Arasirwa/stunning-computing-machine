# 🤝 Contributing Guidelines

Thanks for your interest in contributing to this project! To keep things smooth, organized, and stress-free, please follow the steps below when working on new features, bug fixes, or improvements.

---

## 🧱 Branching Strategy

-   Always branch off of `main`.
-   Use a clear and descriptive naming convention for your branches:
    -   `feature/your-feature-name`
    -   `bugfix/the-bug-being-fixed`
    -   `hotfix/urgent-fix-name`
    -   `chore/refactor-or-maintenance`

---

## 🚀 Development Workflow

1.  **Sync Your `main` Branch**
    Before starting, pull the latest changes from the upstream repository.
    ```bash
    git checkout main
    git pull origin main
    ```

2.  **Create a New Branch**
    Create your new branch from `main` using the naming convention.
    ```bash
    git checkout -b feature/your-feature-name
    ```

3.  **Develop and Commit**
    Write your code and tests. Commit your work in small, logical chunks with clear messages. We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification.
    -   **Examples:**
        -   `feat: add user authentication endpoint`
        -   `fix: resolve null pointer exception in payment processing`
        -   `docs: update contributing guidelines`

4.  **Push Your Changes**
    Push your branch to the remote repository.
    ```bash
    git push origin feature/your-feature-name
    ```

5.  **Open a Pull Request (PR)**
    -   Go to the repository on GitHub and click the **"Compare & pull request"** button.
    -   Fill out the PR template with a detailed description of your changes.
    -   Link any related issues using keywords like `Closes #issue-number` in the description.
    -   Assign at least one reviewer.

6.  **Code Review and Merge**
    -   Your PR requires at least one approval before it can be merged.
    -   Respond to feedback and push any necessary changes. Pushing new commits may reset the approval status.
    -   Once approved, a project maintainer will **squash and merge** your PR into `main`.

---

## 🧹 Branch Cleanup

After your PR is merged, keep our repository tidy by deleting your branches.
1.  **Delete the remote branch:** You can usually do this with the "Delete branch" button on the PR page after it's merged.
2.  **Delete the local branch:** Switch back to `main` and remove the local copy.
    ```bash
    git checkout main
    git branch -d feature/your-feature-name
    ```

---

## 📦 Code Quality

-   **Format your code** using the project's established style guide before pushing.
-   **Write tests** to cover new features and bug fixes.
-   **Ensure all tests pass** locally before opening a pull request.

---

## 💡 Tips

-   Keep your Pull Requests **focused and small**. One feature or bug fix per PR.
-   Use **Draft PRs** to signal work-in-progress and get early feedback.
-   Never commit sensitive information like `.env` files, credentials, or large binaries.

Thanks for helping us build something awesome! 💥
