Git Commands
============

## Translated Versions
- [Versão em português](READMEpt.md)

___

_A list of my commonly used Git commands_

*If you are interested in my Git aliases, have a look at my `.bash_profile`, found here: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

Here’s a list of commonly used Git commands with explanations of what they do:
1. git init
Initializes a new Git repository in the current directory.
bash
Copy code
git init

This sets up the necessary files in the .git directory. After running this command, Git starts tracking changes in the project.
2. git clone <repository-url>
Clones an existing repository from a remote source (e.g., GitHub) to your local machine.
bash
Copy code
git clone https://github.com/user/repo.git

Copies all files and the entire history of the repository to your local system.
3. git status
Displays the state of the working directory and the staging area. It shows changes that have been staged, those that haven’t, and files not being tracked by Git.
bash
Copy code
git status

4. git add <file>
Adds changes in the working directory to the staging area, preparing them to be committed.
bash
Copy code
git add file.txt

git add .: Adds all changes in the current directory to the staging area.
5. git commit -m "message"
Records changes to the repository with a descriptive message of what was done.
bash
Copy code
git commit -m "Added new feature"

The -m option allows you to specify the commit message inline. Without -m, Git opens an editor for writing the message.
6. git push <remote> <branch>
Pushes the changes from your local repository to the remote repository (e.g., GitHub, GitLab).
bash
Copy code
git push origin main

origin: The default name for the remote repository.
main: The branch you want to push changes to.
7. git pull
Fetches changes from a remote repository and merges them into your local branch. It’s a combination of git fetch and git merge.
bash
Copy code
git pull

8. git fetch
Fetches updates from the remote repository, but does not merge them into your local branch. It updates the local copy of the remote branch.
bash
Copy code
git fetch

Useful to see what changes have been made on the remote without affecting your current branch.
9. git branch
Lists, creates, or deletes branches.
bash
Copy code
git branch

Shows all local branches.
git branch <new-branch>: Creates a new branch.
git branch -d <branch>: Deletes a branch.
10. git checkout <branch>
Switches to another branch and updates the working directory to match that branch’s version of the project.
bash
Copy code
git checkout main

git checkout -b <new-branch>: Creates a new branch and switches to it.
11. git merge <branch>
Merges the specified branch into the current branch.
bash
Copy code
git merge feature-branch

Used to incorporate changes from another branch into the current branch.
12. git reset
Resets the current HEAD to a specified state. This command can modify the staging area and working directory based on the option used:
git reset --soft HEAD~1: Moves the HEAD back by one commit, but leaves the working directory and index unchanged.
git reset --hard HEAD~1: Discards the last commit and all changes in the working directory.
13. git log
Shows a list of commits made to the repository.
bash
Copy code
git log

git log --oneline: Shows the commit history as a single line per commit.
14. git rebase
Reapplies commits on top of another base tip, effectively "replaying" changes.
bash
Copy code
git rebase main

Useful when integrating changes from another branch and keeping a clean commit history.
15. git stash
Temporarily saves (stashes) changes that are not ready to be committed. This is useful if you want to switch branches without committing incomplete work.
bash
Copy code
git stash

git stash pop: Restores the stashed changes.
16. git remote add <name> <url>
Adds a new remote repository.
bash
Copy code
git remote add origin https://github.com/user/repo.git

This is typically done after git init to link the local repository to a remote one.
17. git rm <file>
Removes a file from the working directory and the index.
bash
Copy code
git rm file.txt

18. git diff
Shows the differences between the working directory and the staging area.
bash
Copy code
git diff

19. git tag <tagname>
Tags a specific commit with a name, typically used to mark release points.
bash
Copy code
git tag v1.0

20. git config
Configures Git settings (username, email, etc.).
bash
Copy code
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"

21. git revert <commit>
Reverts a specific commit, creating a new commit that undoes the changes.
bash
Copy code
git revert abc123

22. git cherry-pick <commit>
Applies changes from a specific commit to the current branch.
bash
Copy code
git cherry-pick abc123

23. git archive
Creates a zip or tar archive of the repository.
bash
Copy code
git archive --format=zip --output=archive.zip HEAD

Summary of Most Commonly Used Commands:
git init: Initialize a new Git repo.
git clone: Clone a remote repository.
git add: Stage changes for commit.
git commit: Commit staged changes with a message.
git push: Push changes to a remote repository.
git pull: Fetch and merge changes from the remote repository.
git branch: List, create, or delete branches.
git checkout: Switch branches.
git merge: Merge branches.

