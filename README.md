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
- ['README.md' File](#readmemd-file)
- [Pull Request](#pull-requests)
- [Issues](#issues)
  - [Link Issues with Pullrequest](#steps-to-link-an-issue-to-a-pull-request-)
  - [Issue Template](#issue-template)

## What is Git and GitHub?

### **Git**

> _Git_ is a distributed version control system that tracks changes to files and coordinates work on those files among multiple people. It allows for local and remote repositories, branching, and merging, enabling efficient and collaborative development.

## **GitHub**

> _GitHub_ is a web-based platform that hosts Git repositories, providing tools for version control, collaboration, and project management. It includes features like pull requests, issues, and CI/CD integration, enhancing team workflows and code sharing.

## Git vs GitHub

| Feature             | Git                                                                    | GitHub                                                                            |
| ------------------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Definition          | Distributed version control system for tracking changes in source code | Web-based platform for hosting Git repositories and collaborating on projects     |
| Main Purpose        | Version control and source code management                             | Repository hosting, collaboration, and project management                         |
| Initial Release     | 2005                                                                   | 2008                                                                              |
| Hosting             | Local and remote repositories                                          | Remote repositories                                                               |
| Interface           | Command-line interface                                                 | Web-based interface with integrations to other tools and services                 |
| Additional Features | Branching, merging, rebasing, and more                                 | Pull requests, issues, project boards, GitHub Actions for CI/CD, and more         |
| Authentication      | SSH keys, HTTPS, and CLI                                               | Personal access tokens, OAuth, SSH keys, and SAML                                 |
| Integration         | Can be integrated with various CI/CD tools manually                    | Built-in CI/CD with GitHub Actions, integrates with many other tools and services |

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

- It Uses cryptographic keys for secure communication between your local machine and the remote server.

```sh
git clone git@github.com:user/repository.git
```

### HTTPS

- Uses the standard HTTP protocol with encryption, requiring a username and password (or a personal access token) for each interaction with the remote repository.

```sh
git clone https://github.com/user/repository.git
```

### CLI (Command-Line Interface)

- The tool you use to issue Git commands through your terminal or command prompt.

```sh
git clone [repository_url]
git commit -m "Commit message"
git push origin main
```

#

## **.gitignore** File

The `.gitignore` file is a configuration file used by Git to specify which files and directories should be ignored and not tracked by version control.

## README.md File

A **README** file is an markdown file`(.md)` used to provide an overview of the project, including installation instructions, usage guidelines, and contribution information. It serves as the primary source of documentation for users and contributors. It helps in quickly understanding the project's purpose and how to get started with it.

## **Pull Requests**

A **Pull Request (PR)** is a method of submitting contributions to a project. It allows developers to notify project maintainers about changes they'd like to merge into the main codebase.

## **Issues**

- **Issues** on GitHub are used to track tasks, enhancements, bugs, and other project-related work. They allow users and contributors to discuss and collaborate on these topics. Each issue can be tagged, assigned, and referenced in commits and pull requests to streamline project management.

## Steps to Link an Issue to a Pull Request :

**Create or identify the issue:**

- Open or find an existing issue you want to address.

**Create a pull request:**

- Make your changes in a new branch.
- Push the branch to your GitHub repository.
- Open a pull request and include a description.

**Link the issue:**

- In the PR description, use keywords like `Fixes #42`, `Closes #42` or `Resolves #42` to link and automatically close issue #42 when the PR is merged.

## **Issue Template**

### 1. Creating an Issue Template :

GitHub allows you to create issue templates that users can fill out when they create a new issue.you need to create a markdown file `bug_report.md` to define the template of your github isuue's template.

Header contents of `ISSUE_TEMPLATE/bug_report.md` file

```sh
---
name: Bug Report
about: Create a report to help us improve
title: "[BUG] "
labels: bug
assignees: ''
----
```

### 2. Creating the Configuration File :

A configuration file can be used to further customize the behavior of issue templates and forms using `config.yml` file.

```sh
  - name: "Support"
    url: "https://example.com/support"
```

### 3. Setting Up the Templates in Your Repository :

```
.github/
└── ISSUE_TEMPLATE/
   ├── bug_report.md
   └── config.yml
```
