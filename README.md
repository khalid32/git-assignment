# Git Advanced Workflow Assignment

# Enterprise-Level Git Workflow Assignment

## 📌 Commands Used
Here is a log of the core Git commands utilized to complete this project:
* `git init` - Initialized the local repository.
* `git branch <branch-name>` - Created feature and bugfix branches.
* `git switch <branch-name>` - Navigated between branches.
* `git merge <branch-name>` - Integrated changes using the fast-forward merge strategy.
* `git rebase <base-branch>` - Reapplied commits on top of another base tip for a linear history.
* `git rebase -i HEAD~5` - Initiated an interactive rebase to squash and reword commits.
* `git push -u origin <branch-name>` - Pushed local branches to the remote GitHub repository.

## 🧠 Concepts Explained

### Merge vs. Rebase
* **Merge:** Merging integrates changes from one branch into another by preserving the exact history of both, often creating a new "merge commit" to tie the two timelines together.
* **Rebase:** Rebasing rewrites project history by moving the entire feature branch to begin at the current tip of the target branch, resulting in a clean, linear history without extra merge commits.

### Squash & Reword
* **Squash:** Squashing is a history manipulation technique that condenses multiple small, messy, or "work-in-progress" commits into a single, cohesive commit to keep the main branch readable.
* **Reword:** Rewording allows you to modify the text of a previous commit message without changing the underlying code, ensuring the final project history is professional and descriptive.