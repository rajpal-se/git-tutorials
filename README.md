<!-- markdownlint-disable MD001 MD014 MD024 MD031 -->

# Git Commands

#### Initializing a Repository

- `git init .`: Initialize a new Git repository in the current directory.

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

---

# Examples

##### Initializing a Repository

- `git init .`: Initializes a new Git repository in the current directory.
Example:
    ```bash
    $ git init .
    # Initialized empty Git repository in /path/to/repository/.git/
    ```

##### Basic Snapshotting

- `git add <file>`: Adds a file or changes to the staging area.
    Example:
    ```bash
    $ git add myfile.txt
    
    # To add files in current directory
    $ git add .
    ```

- `git commit -m "<message>"`: Commits staged changes to the repository with a descriptive message.
    Example:
    ```bash
    $ git commit -m "Added new feature"
    # [master abcdef1] Added new feature
    #   1 file changed, 2 insertions(+)
    ```

- `git status`: Shows the status of modified files in the working directory.

    Example:
    ```bash
    $ git status
    # On branch master
    # Your branch is up to date with 'origin/master'.
    #
    # Changes not staged for commit:
    #   (use "git add <file>..." to update what will be committed)
    #   (use "git restore <file>..." to discard changes in working directory)
    #         modified:   myfile.txt

    # no changes added to commit (use "git add" and/or "git commit -a")
    ```

- `git diff`: Shows changes between the working directory and the staging area.

    Example:
    ```bash
    $ git diff myfile.txt
    # diff --git a/myfile.txt b/myfile.txt
    # index 1234567..abcdefg 100644
    # --- a/myfile.txt
    # +++ b/myfile.txt
    # @@ -1,3 +1,5 @@
    #  Hello, world!
    # +This is a new line.
    #  Another line.
    #  Goodbye!
    ```

##### Branching and Merging

- `git branch`: Lists all branches in the repository.

    Example:
    ```bash
    $ git branch
    # * master
    #   feature/branch1
    #   feature/branch2
    ```

- `git branch <branch-name>`: Creates a new branch.
    Example:
    ```bash
    $ git branch feature/new-feature
    ```

- `git checkout <branch-name>`: Switches to an existing branch.

    Example:
    ```bash
    $ git checkout development
    # Switched to branch 'development'
    $ git checkout main
    # Switched to branch 'main'
    ```

- `git checkout -b <branch-name>`: Create a new branch from current branch and Switch to the new branch.

    Example:
    ```bash
    $ git checkout -b bug/fix-email-validation
    # Switched to a new branch 'bug/fix-email-validation'
    ```

- `git merge <branch-name>`: Merges changes from one branch into the current branch.

    Example:
    ```bash
    $ git merge feature/branch1
    # Updating abcdef1..1234567
    # Fast-forward
    #     myfile.txt | 2 +-
    #     1 file changed, 1 insertion(+), 1 deletion(-)
    ```

- `git stash`: Stashes changes in a dirty working directory for later use.

    Example:
    ```bash
    $ git stash
    # Saved working directory and index state WIP on feature/new-feature: 1234567 Added new feature
    ```

##### Remote Repositories

- `git remote add <name> <url>`: Adds a remote repository.

    Example:
    ```bash
    $ git remote add origin https://github.com/user/repo.git
    ```

- `git push <remote> <branch>`: Pushes changes to a remote repository.

    Example:
    ```bash
    $ git push origin master
    ```

- `git pull <remote> <branch>`: Fetches and merges changes from a remote repository.

    Example:
    ```bash
    $ git pull origin master
    ```

- `git clone <url>`: Clones a remote repository to a local machine.
  `git clone <url> .`: Clones into the current folder

    Example:
    ```bash
    $ git clone https://github.com/user/repo.git
    # Cloning into 'repo'...
    # remote: Enumerating objects: 100, done.
    # remote: Counting objects: 100% (100/100), done.
    # remote: Compressing objects: 100% (80/80), done.
    # Receiving objects: 100% (100/100), 10.00 KiB | 5.00 MiB/s, done.
    # Resolving deltas: 100% (20/20), done.
    ```

##### Inspecting History

- `git log`: Shows commit history.

    Example:
    ```bash
    $ git log
    # commit abcdef1
    # Author: John Doe <john.doe@example.com>
    # Date:   Tue May 1 12:00:00 2023 +0300
    #
    #     Added new feature
    #
    # commit 1234567
    # Author: John Doe <john.doe@example.com>
    # Date:   Mon Apr 30 09:30:00 2023 +0300
    #
    #     Updated README.md
    ```

- `git show <commit>`: Shows details of a specific commit.

    Example:
    ```bash
    $ git show abcdef1
    # commit abcdef1
    # Author: John Doe <john.doe@example.com>
    # Date:   Tue May 1 12:00:00 2023 +0300
    #
    #     Added new feature
    #
    # diff --git a/myfile.txt b/myfile.txt
    # index 1234567..abcdefg 100644
    # --- a/myfile.txt
    # +++ b/myfile.txt
    # @@ -1,3 +1,5 @@
    #  Hello, world!
    # +This is a new line.
    #  Another line.
    #  Goodbye!
    ```

- `git blame <file>`: Shows who modified each line of a file.

    Example:
    ```bash
    $ git blame myfile.txt
    abcdef1 (John Doe 2023-05-01 12:00:00 +0300 1) Hello, world!
    abcdef1 (John Doe 2023-05-01 12:00:00 +0300 2) This is a new line.
    1234567 (John Doe 2023-04-30 09:30:00 +0300 3) Another line.
    abcdef1 (John Doe 2023-05-01 12:00:00 +0300 4) Goodbye!
    ```

##### Undoing Changes

- `git revert <commit>`: Creates a new commit that undoes the changes made in a specific commit.

    Example:
    ```bash
    $ git revert abcdef1
    # [master 9876543] Revert "Added new feature"
    #  1 file changed, 2 deletions(-)
    ```

- `git reset`: Resets the staging area and working directory to a previous commit.

    Example:
    ```bash
    $ git reset --hard 1234567
    # HEAD is now at 1234567 Updated README.md
    ```

- `git checkout -- <file>`: Discards changes made to a file in the working directory.

    Example:
    ```bash
    $ git checkout -- myfile.txt
    ```
