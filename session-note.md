# Essential Git Commands

### Navigating and Checking Status

- git status = Check the current status of your repository (modified, untracked files, etc.)
- git branch = List all branches and see which one you're on
- git log --oneline --graph = View commit history in a compact format
- git show <commit-hash> # View details of a specific commit

### Working with Branches

- git branch <branch-name> = Create a new branch
- git switch <branch-name> = Switch to an existing branch
- git switch -c <branch-name> = Create and switch to a new branch
- git checkout -b <branch-name> = (Alternative) Create and switch to a new branch
- git branch -d <branch-name> = Delete a local branch
- git push origin --delete <branch> = Delete a remote branch

### Committing and Saving Changes

- git add <file> = Stage a specific file
- git add . = Stage all modified and new files
- git commit -m "Commit message" = Commit staged files with a message
- git commit --amend -m "New message" = Edit the last commit message
- git reset HEAD <file> = Unstage a file before committing
- git restore --staged <file> = Also unstages a file before committing

### Pushing & Pulling from GitHub

- git push origin <branch> = Push local changes to GitHub
- git push --set-upstream origin <branch> = Push a new branch to GitHub and set it as upstream
- git pull origin <branch> = Fetch and merge changes from the remote branch
- git fetch origin = Fetch changes without merging them
- git fetch --prune = Remove deleted remote branches from your local repository

### Merging & Rebasing

- git merge <branch> = Merge another branch into the current one
- git rebase <branch> = Reapply commits from one branch onto another
- git merge --abort = Cancel a merge if there are conflicts
- git rebase --abort = Cancel a rebase if there are issues

### Undoing Changes

- git checkout -- <file> = Discard local changes (before staging)
- git reset --soft HEAD~1 = Undo the last commit but keep changes staged
- git reset --hard HEAD~1 = Undo the last commit and discard all changes
- git revert <commit-hash> = Create a new commit that undoes a specific commit

### Cloning, Forking & Managing Repos

- git clone <repo-url> = Clone a repository
- git remote -v = View the remote repositories linked
- git remote add origin <repo-url> = Add a remote repository
- git remote remove <name> = Remove a remote repository
- git fork = (Done via GitHub UI) Fork a repository

### Stashing Temporary Changes

- git stash = Save uncommitted changes temporarily
- git stash list = Show list of stashed changes
- git stash apply = Reapply the last stashed changes
- git stash pop = Apply and remove the stash
- git stash drop = Delete the last stashed change

### Checking Differences

- git diff = Show changes in unstaged files
- git diff --staged = Show changes in staged files
- git diff <commit1> <commit2> = Show differences between two commits

### Shortcuts & Useful Flags

- git log --oneline --graph --all = Visualize the commit history
- git config --global user.name "Your Name" = Set your Git username
- git config --global user.email "you@example.com" = Set your Git email

## Common Scenarios & Solutions

"I modified a file but don't want to commit it yet"

git checkout -- <file>

"I made a mistake in my last commit message"

git commit --amend -m "New message"

"I want to undo my last commit but keep the changes"

git reset --soft HEAD~1

"I want to delete a local branch"

git branch -d <branch>

"I want to force delete a local branch"

git branch -D <branch>

"I want to delete a remote branch"

git push origin --delete <branch>

"I forgot to pull before pushing, now I have conflicts"

git pull --rebase origin main
