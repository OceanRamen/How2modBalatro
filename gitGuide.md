# OceanRamen's Git Guide

## 1. **Getting Started with Git**

- **Installation**

  - To start using Git, install it from the [official website](https://git-scm.com/downloads).
  - After installation, configure your name and email with:

    ```bash
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    ```

- **Creating a Repository**

  - Navigate to your project directory and initialize a new Git repository:

    ```bash
    git init
    ```

  - This creates a `.git` directory where Git tracks changes.

- **Cloning a Repository**

  - To copy an existing Git repository:

    ```bash
    git clone https://github.com/user/repo.git
    ```

  - Replace the URL with the repository you want to clone.

## 2. **Basic Commands**

- **Checking the Status**

  - To see the current state of your working directory and staging area:

    ```bash
    git status
    ```

  - This shows which files are modified, staged for commit, or untracked.

- **Adding Changes**

  - To stage changes for commit:

    ```bash
    git add filename
    ```

  - To stage all changes:

    ```bash
    git add .
    ```

- **Committing Changes**

  - To save your staged changes with a message:

    ```bash
    git commit -m "Your commit message"
    ```

  - Make your commit messages clear and descriptive.

## 3. **Viewing History**

- **Viewing Commit History**

  - To see the commit history:

    ```bash
    git log
    ```

  - This shows a detailed list of commits.

- **Viewing a Compact Log**

  - To view a concise version of your commit history with a graphical representation:

    ```bash
    git log --graph --oneline
    ```

  - This is useful for quickly understanding the commit structure.

## 4. **Branching and Merging**

- **Creating a Branch**

  - To create a new branch:

    ```bash
    git branch branch-name
    ```

  - Switch to the new branch:

    ```bash
    git checkout branch-name
    ```

- **Merging Branches**

  - To merge changes from another branch into your current branch:

    ```bash
    git merge branch-name
    ```

  - This integrates the changes from `branch-name` into the branch you're currently on.

- **Rebasing Branches**

  - To rebase your branch onto another branch (replay your changes on top of another branch):

    ```bash
    git checkout your-branch
    git rebase branch-name
    ```

  - Rebasing creates a cleaner history but can be complex. Use with caution.

> [!NOTE]
> You should always perform rebasing and merging on new branches. This will save you a lot of headache in the future.

## 5. **Advanced Commands**

- **Viewing Branches**

  - To see a list of all branches:

    ```bash
    git branch
    ```

  - To see a visual representation of your branches:

    ```bash
    git log --graph --oneline --all
    ```

- **Stashing Changes**

  - To temporarily save changes without committing them:

    ```bash
    git stash
    ```

  - To apply the stashed changes:

    ```bash
    git stash apply
    ```

## 6. **Undoing Changes**

- **Discarding Unstaged Changes**

  - To discard changes in your working directory:

    ```bash
    git checkout -- filename
    ```

  - Be careful; this will permanently delete your changes.

- **Resetting Commits**

  - To move back to a previous commit and discard all subsequent changes:

    ```bash
    git reset --hard commit-hash
    ```

  - Replace `commit-hash` with the desired commit identifier from `git log`.

## 7. **Version Control Best Practices**

- **Commit Often**

  - Make small, frequent commits with clear messages.

- **Use Branches**

  - Keep your work organized by using branches for new features or fixes.

- **Review Before Merging**

  - Always review changes before merging to avoid conflicts.

## 8. **Pushing and Pulling**

- **Pushing Changes**

  - To upload your commits to a remote repository:

    ```bash
    git push origin branch-name
    ```

  - Replace `branch-name` with the branch you're pushing.

- **Pulling Changes**

  - To fetch and integrate changes from a remote repository:

    ```bash
    git pull origin branch-name
    ```

## 9. **Conclusion**

- Git is a powerful tool for managing your code. Regularly practice these commands to become proficient. Remember to always keep your commit messages clear and your branches organized.
