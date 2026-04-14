# Git Advanced Workflow Assignment

# Enterprise-Level Git Workflow Assignment

## 📌 Commands Used
Here is a log of the core Git commands utilized to complete this specific workflow:

**Repository & Branch Initialization:**
* `git config --global user.name "Khalid"` - Configured local Git profile.
* `git init` - Initialized the local repository.
* `git branch -M main` - Set the default branch name.
* `git branch <branch-name>` - Created the `develop`, `feature/login`, `feature/payment`, and `bugfix/login-error` branches.
* `git switch -c feature/profile` - Created and immediately switched to the profile feature branch.

**Staging & Committing:**
* `git add <file>` - Staged newly created and modified files.
* `git commit -m "<message>"` - Created standard commits for features and documentation.

**Merging & Rebasing (Integration):**
* `git merge feature/login` - Integrated the login feature into `develop` using a fast-forward merge strategy.
* `git rebase develop` - Rebased the `feature/payment` branch onto `develop` to maintain a clean, linear history before integrating.

**History Manipulation:**
* `git config --global core.editor "code --wait"` - Set VS Code as the default editor for interactive Git commands.
* `git rebase -i HEAD~5` - Initiated an interactive rebase to squash 5 "work-in-progress" commits into a single feature commit.
* `git commit --amend -m "<message>"` - Overwrote the most recent commit message to finalize the reword process.
* `git rebase --quit` - Safely aborted and cleared a locked rebase state.

**Remote Repository (GitHub):**
* `git remote add origin <url>` - Linked the local repository to the remote GitHub repository.
* `git push -u origin main` - Pushed the main branch and established upstream tracking.
* `git push origin <branches>` - Pushed all remaining feature, develop, and bugfix branches to the remote.

## 🧠 Concepts Explained

### Merge vs. Rebase
* **Merge:** Merging integrates changes from one branch into another by preserving the exact history of both, often creating a new "merge commit" to tie the two timelines together.
* **Rebase:** Rebasing rewrites project history by moving the entire feature branch to begin at the current tip of the target branch, resulting in a clean, linear history without extra merge commits.

### Squash & Reword
* **Squash:** Squashing is a history manipulation technique that condenses multiple small, messy, or "work-in-progress" commits into a single, cohesive commit to keep the main branch readable.
* **Reword:** Rewording allows you to modify the text of a previous commit message without changing the underlying code, ensuring the final project history is professional and descriptive.