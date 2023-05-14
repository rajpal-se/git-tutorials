<!-- markdownlint-disable MD001 -->

# Git Commands

#### Initializing a Repository

- `git init`: Initialize a new Git repository in the current directory.

#### Basic Snapshotting

- `git add <file>`: Add a file or changes to the staging area.
- `git commit -m "<message>"`: Commit staged changes to the repository with a descriptive message.
- `git status`: Show the status of modified files in the working directory.
- `git diff`: Show changes between the working directory and the staging area.

#### Branching and Merging

- `git branch`: List all branches in the repository.
- `git branch <branch-name>`: Create a new branch.
- `git checkout <branch-name>`: Switch to an existing branch.
- `git merge <branch-name>`: Merge changes from one branch into the current branch.
- `git stash`: Stash changes in a dirty working directory for later use.

#### Remote Repositories

- `git remote add <name> <url>`: Add a remote repository.
- `git push <remote> <branch>`: Push changes to a remote repository.
- `git pull <remote> <branch>`: Fetch and merge changes from a remote repository.
- `git clone <url>`: Clone a remote repository to a local machine.

#### Inspecting History

- `git log`: Show commit history.
- `git show <commit>`: Show details of a specific commit.
- `git blame <file>`: Show who modified each line of a file.

#### Undoing Changes

- `git revert <commit>`: Create a new commit that undoes the changes made in a specific commit.
- `git reset`: Reset the staging area and working directory to a previous commit.
- `git checkout -- <file>`: Discard changes made to a file in the working directory.
