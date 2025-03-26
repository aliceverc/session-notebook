## Your First Steps with Git!

Git is like a time machine for your code! It helps you keep track of all the changes you make. Here are some key commands to get you going:

**Starting Your Git Journey:**

- `git init`: Use this command to turn your current folder into a Git project.
- `git clone`: If someone else has already started a Git project online, you can use this to bring a copy of it to your computer.

**Saving Your Amazing Work:**

- `git add`: This is like staging your changes – telling Git "Hey, remember these updates!"
- `git commit -m "Describe your changes here!"`: This saves a snapshot of your staged changes. Make sure to write a clear message so you know what you did!
- **The `.gitignore` File:** This handy file lets you tell Git to ignore certain files that you don't need to track, like temporary files or personal settings.

**Sharing and Collaborating (Remote Repositories):**

- `git push`: Ready to share your work? This command sends your saved snapshots to an online repository.
- `git pull`: Need to get the latest updates from the online repository? This command brings those changes to your computer.

**Exploring Your Project's History:**

- `git log`: Want to see all the snapshots that have been taken? This command shows you the history of your project.
- `git status`: Curious about what's changed in your project right now? This command gives you a quick overview.

**Things to Keep in Mind:**

- Git doesn't track empty folders, so don't worry if they don't show up!
- It's best to keep your Git projects separate – one inside another can cause confusion.

**Understanding the `.gitignore` File:**
You'll usually create this file in the main folder of your project. Inside, you simply list the names of files or patterns of files that you want Git to ignore. Once a file is in this list, Git will leave it alone, no matter where it is in your project.

Git CLI & remote
Learning Objectives

    - using version control locally to create repositories and commits
    - understanding different states of files
    - synchronizing local repositories with remote repositories

Git CLI

You can create git repositories and commits locally. You can also synchronize your local repository with a remote repository (i.e. on GitHub).

Creating local repositories

To turn a folder into a git repository you need the following git command:

    cd path/to/my/folder
    git init

❗️ Do not initialize a git repository inside another git repository!
To check if a folder has already been initialized you can run the following git command

    git status

Not a git repo:

    fatal: not a git repository (or any of the parent directories): .git

A git repo:

    On branch main
    nothing to commit, working tree clean

States of files

On GitHub, we can create, modify and delete files, the same can be done via the terminal. To understand how this works, we have to know about the different states a file can have.
Untracked files

The file has not been added to git.
Tracked files

Tracked files can be in different states:
state description
modified Has changes since the last commit
staged Is included in the next commit
committed All changes have been saved in git
Committing in a local repository

We recommend executing the following git commands for every completed task:

    💡 Hint: Commits help track your progress.
    Commit early, commit often.
    Make sure, that your code works as expected.

Git command Git task
git status List all files that have changed and their state
git add <filename> Add a file to the stage
git commit -m "add foo" Create a commit including all staged files
git log --oneline Show the commit history

untracked to committed

modified to committed
Using commits as backups

You can always return to the last committed state of the entire project:

git restore .

You can also restore individual files:

git restore <filename>

Connecting to a remote repository

This enables teams to work on the same remote repository and clone it locally. The remote repository also serves as a backup.
Connecting your local repository to a new remote repository

The first thing you need to do is create a new empty remote repository on GitHub. You will then see some hints e.g. "...or push an existing repository from the command line". Copy the commands from GitHub and execute them in your local project folder.

Example:

git remote add origin git@github.com:GitHubUsername/repository-name.git
git branch -M main
git push -u origin main

Cloning a remote repository

You can create a copy of the remote repository on your local machine with the following command:

git clone <url>

    💡 You can find the url of remote repositories on GitHub on the repository page. Please use the SSH url.

Clone SSH
Synchronizing local & remote repositories
Git command Git task
git push Upload content to the remote repository
git pull Download content from the remote repository
