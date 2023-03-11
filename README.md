# Git-Commands-Cheat-Sheet
_A list of commonly used Git commands_

___


### Git Setup & Configuration Globally
| Command | Description |
| ------- | ----------- |
| `git config --global user.name "<your username>"` | Setup your Git username |
| `git config --global user.email "<your email>"` | Setup your Git email address |
| `git config --global credential.helper cache` | Caching your login credentials in Git |


### Git help
| Command | Descripton |
| ------- | ---------- |
| `git <command> help` | See available options for a specific command |
| `git help --all` | See all possible commands |


### Getting & Creating Projects
| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone <ssh://git@github.com/[username]/[repository-name].git>` | Create a local copy of a remote repository |


### Basic Snapshotting
| Command | Description |
| ------- | ----------- |
| `git status [--short]` | Check the status of repo |
| `git add <file-name>` | Add a file to the staging area |
| `git add -A` or `git add .` or `git add *` or `git add --all` | Add all new and changed files to the staging area |
| `git add -p` | Opens a prompt and asks if you want to stage changes or not |
| `git add fil*` | Add all new and changed files starting with 'fil' to the staging area |
| `git commit` | Commit changes in the editor |
| `git commit -m "<commit message>"` | Commit changes with a short message |
| `git commit -a -m "<commit message>"` | Commit changes with a short message skipping the staging environment |
| `git rm -r <file-name.txt>` | Remove a tracked file (or folder) |
| `git mv <old name> <new name>` | Rename the file |


### Rollbacks
| Commands | Description |
| -------- | ----------- |
| `git checkout <filename>` | Revert unstaged changes |
| `git reset HEAD <filename>` | Revert staged changes |
| `git reset HEAD -p` | Specify the changes you want to reset |
| `git commit --amend` | Overwrite the most recent commit (it is great locally, but avoid it in public) |
| `git revert HEAD` | Rollback the last commit |
| `git revert <commit-id>` | Rollback to a specific old commit |


### Branching & Merging
| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch -r` | Check remote branches that Git is tracking |
| `git branch <branch name>` | Create a new branch |
| `git branch -d <branch name>` | Delete a branch |
| `git push origin --delete <branch name>` | Delete a remote branch |
| `git checkout -b <branch name>` | Create a new branch and switch to it |
| `git checkout -b <branch name> origin/<branch name>` | Clone a remote branch and switch to it |
| `git branch -m <old branch name> <new branch name>` | Rename a local branch |
| `git checkout <branch name>` | Switch to a branch |
| `git checkout` | Switch to the branch last checked out |
| `git merge <branch name>` | Merge a branch into the active branch (preferred to switch to it) |
| `git merge <source branch> <target branch>` | Merge a branch into a target branch |
| `git merge --abort` | Abort a conflicting merge |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git rebase <branch name>` | Transfer work from one branch to another |


### Sharing & Updating Projects
| Command | Description |
| ------- | ----------- |
| `git push origin <branch name>` | Push a branch to your remote repository |
| `git push -u origin <branch name>` | Push changes to remote repository (and remember the branch) |
| `git push [-f]` | [Force] push changes to remote repository (remembered branch) |
| `git push origin --delete <branch name>` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin <branch name>` | Pull changes from remote repository |
| `git remote add origin <ssh://git@github.com/[username]/[repository-name].git>` | Add a remote repository |
| `git remote set-url origin <ssh://git@github.com/[username]/[repository-name].git>` | Set a repository's origin branch to SSH |
| `git remote -v` | See all remote repositories for local repository |


### Inspection & Comparison
| Command | Description |
| ------- | ----------- |
| `git log` | View commit history |
| `git log -p` | View commit history with changes |
| `git log --stat` | Show statistics in each commit including line(s) changed |
| `git log --summary` | View changes (detailed) |
| `git log --oneline --graph --all` | View changes (briefly in single line) graphically for all branches |
| `git log origin/main` | Check the current commits log of a remote repo |
| `git show <commit-id>` | View a specific commit |
| `git diff <source branch> <target branch>` | Preview changes before merging |
| `git diff --staged` | See any staged changes |
