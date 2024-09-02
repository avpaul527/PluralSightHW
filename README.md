# PluralSightHW
Git Fundamentals (Notes) | Alexandria Paul
-Course reviews foundations of Git. Course goes over how to think in Git, Install and set up locally, Working in a shared environment, and alter and reset changes.
-Most widely used version control system in the world today. It is free and open source.
- Git allows you to version control any type of file, not just open source code. Helps to track changes. Centralized, distributed, and advanced version control system for efficient collaboration.
- Chracteristics of Git: Delta's are differences in each file version, represented by snapshots in Git. Git is optimized for local development. Git is explicit in terms of you clearly giving it instructions to follow. Git is designed for non-linear development. A new branch in Git is a pointer to a different snapshot.
- Two states of files is untracked and tracked. Tracked is from the latest snapshot of your project. Tracked states: Unmodified, Modified, and Staged. Unmodified directory = .git/Directory. Modified directory = Working directory. Staged directory = Cache/Index/Staging directory.
- Over 150 different Git commands. Repository = Git project. git (command) --help will give info on each command.
- Git basics commands = git init, git add, git status, git commit, git config, git log, git diff
- Git branches commands = git branch, git checkout, git merge
- Remote repositories commands = git clone, git remote, git push, git pull, git fetch
- Undoing changes commands = git revert, git reset
- Can use local terminals, but Git Bash is recommended.
- Creating a repository: mkdir (projectname). cd [projectname). git init. git branch -m main [changes from "master" to "main"]. git init [reinitializes]. [DO NOT DELETE .git DIRECTORY!]. git status.
- Configuration levels: --system, --global, --local
- For user: git config --global user.name "(username)". git config --global user.email "(email address)". git config --global --list [will show current configured default user]. git config --global init.defaultBranch main [to change from 'master' to 'main']. git config --global --unset (setting) [to remove last setting].
- code . [opens up Visual Studio Code]. Code/View/Command Pallete, Shell Command: Install code command in PATH. [You can make changes to files this way.]
- git add . [adds all files in directory]. git reset [if you want to undo and add each file manually]. Then, git add (name of file) (name of file2) (etc.). git status [to show added files]. git commit -m "Message" [AFTER you confirm the files added are correct].
- Creating another branch: git branch (name). git branch -a [shows local branches]. git checkout (name) [switches to branch]. git checkout -b (name) [creates and switches to branch at the same time].
- git diff [changes in working directory]. git diff --staged [in index]. git diff head [changes in both].
- git merge (branch name) -m "Message" [merges branch to main].
- git log [displays all commits]. press "q" [to return to command line]. git log  --oneline [simplifies display of commits to one line each]. git log --oneline --graph [one line commits with visual representation]. git branch -d (branch name) [deletes a branch]. git branch -a [lists all branches].
- Create repository on GitHub:
- New Repository on commandline: echo "# (repo name)" >> README.md, git init, git add README.md, git commit -m "first commit", git branch -M main, git remote add origin https://github.com/(link to your repo...)/, git push -u origin main
- Push existing Repository from commandline: git remote add origin https://github.com/(link to your repo...)/, git branch -M main, git push -u origin main
- Cloning a repo: git clone https://github.com/(link to your repo...)/. [remember to 'cd' into repo to interact, you can make changes to repo, then 'commit' and 'push']. git pull [to retrieve changes that have been pushed by others]. git pull = git fetch + git merge.
- Merge conflict - occurs when there are conflicting changes being introduced to the same contents in the same file. If 'git merge' returns CONFLICTs, 'git status' will provide some options on how to resolve mentioned conflicts. Editing the file will show both your changes and conflicting changes, and you can choose which changes to keep, then save. git add, git commit, and git push to resolve.
- git commit --amend [to fix/change commit message]. note: commit ID will change.
- git reset - git reset --soft, git reset --mixed [also known as git reset], git reset --hard. To commit resets, git add, git commit. git reset --hard [throws away all commits that have not been pushed.] git reflog [restore previous commited changes local, only available for commits for 90 days]. git cherry-pick (commit ID from git reflog) [places back into commit history].
- Git Workflows - Basic Workflow [one branch, small & simple commits], Feature Branch Workflow [utilizes another branch for changes], & Git Flow [like Feature Branch Workflow, but utilizes Develop branch rather than immediately into main branch].
- Basic Workflow: main branch
- Feature Branch Workflow: feature branch, main branch
- Git Flow: feature branch, develope branch, main branch.
-----------------------------------------------------------------------------
