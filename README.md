# Github-Examples

- [Git and GitHub](#what-is-git-and-github)
  - [Git](#git)
  - [Github](#github)
- [Fundamental Actions using Git](#fundamental-actions-using-git)
- [Installation of Git and Github Desktop](#installation-of-git-and-github-desktop)
- [Git Basic Commands](#git-basic-commands)
  - [Initializing a Repo](#initializing-a-repo)
  - [Dealing with Branches](#dealing-with-branches)
  - [Updating the Changes](#updating-the-changes)
  - [Update Remote Repository](#update-remote-repository)
  - [Viewing History](#viewing-history)
  - [Handling Conflicts](#handling-conflicts)
- [Git: SSH vs HTTPS vs CLI](#git-ssh-vs-https-vs-cli)
  - [SSH (Secure Shell)](#ssh-secure-shell)
  - [HTTPS](#https)
  - [ GitHub CLI (Command Line Interface)](#cli-command-line-interface)
- ['.gitignore' File](#gitignore-file)

## What is Git and GitHub?

### **Git**

> _Git_ is a distributed version control system that tracks changes to files and coordinates work on those files among multiple people. It allows for local and remote repositories, branching, and merging, enabling efficient and collaborative development.

## **GitHub**

> _GitHub_ is a web-based platform that hosts Git repositories, providing tools for version control, collaboration, and project management. It includes features like pull requests, issues, and CI/CD integration, enhancing team workflows and code sharing.

## Fundamendatal actions using Git

> <strong>Clone</strong>: Create a local copy of a remote repository from the Github.<br> <strong>Commit</strong>: Save changes to the local repository with a message describing the changes in form of tree.<br> <strong>Push</strong>: Upload local commits to a remote repository.<br> <strong>Pull</strong>: Fetch and merge changes from a remote repository to the local repository.<br> <strong>Branch</strong>: Create a separate line of development used to mulitple ways of development of the same repository at the same time .<br> <strong>Merge</strong>: Combine changes from different branches after dealing with conflicts to main branch.<br> <strong>Fork</strong>: Create a personal copy of someone else's repository on GitHub.<br><strong>Issues</strong>: Track bugs, enhancements, or tasks related to the project.<br>

## Installation of Git and Github Desktop

### To install Git on **Windows** :

```sh
https://git-scm.com
```

### To install Git on **Linux** :

```sh
$ sudo dnf install git-all
```

### To install **Github_Desktop**:

```sh
https://github.com/apps/desktop
```

# Git Basic Commands

## Initializing a Repo

- `git init`: Initialize a new Git repository.
- `git clone [repository_url]`: Clone an existing remote repository to your local machine.

## Dealing with Branches

- `git branch`: List all branches in the repository.
- `git branch [branch_name]`: Create a new branch.
- `git checkout [branch_name]`: Switch to a different branch.
- `git merge [branch_name]`: Merge a branch into the current branch.

## Updating the Changes

- `git status`: Show the status of changes as untracked, modified, or staged.
- `git add [file_name]`: Stage changes for the next commit.
- `git add .`: Stage all changes in the current directory.
- `git commit -m "[commit_message]"`: Commit staged changes with a descriptive message.

## Update Remote Repository

- `git push`: Push local changes to the remote repository.
- `git pull`: Fetch and merge changes from the remote repository to your local repository.
- `git fetch`: Fetch changes from the remote repository without merging.

## Viewing History

- `git log`: Show commit history.

## Handling Conflicts

- `git merge [branch_name]`: Merge changes from one branch to another.

##

# Git: SSH vs HTTPS vs CLI

### SSH (Secure Shell):

> Uses cryptographic keys for secure communication between your local machine and the remote server.

```sh
git clone git@github.com:user/repository.git
```

### HTTPS

> Uses the standard HTTP protocol with encryption, requiring a username and password (or a personal access token) for each interaction with the remote repository.

```sh
git clone https://github.com/user/repository.git
```

### CLI (Command-Line Interface)

> The tool you use to issue Git commands through your terminal or command prompt.

```sh
git clone [repository_url]
git commit -m "Commit message"
git push origin main
```

#

## **.gitignore** File

> The `.gitignore` file is a configuration file used by Git to specify which files and directories should be ignored and not tracked by version control.
