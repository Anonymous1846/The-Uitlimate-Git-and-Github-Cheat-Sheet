# Git and GitHub: From Beginner to Master [2024]

Welcome to the comprehensive guide on mastering Git and GitHub. This guide will take you through the most beginner to advanced topics, helping you become proficient in version control,collaborative and open source development.

## Table of Contents
1. [Introduction to Git](#introduction-to-git)
2. [Setting Up Git](#setting-up-git)
3. [Basic Git Commands](#basic-git-commands)
4. [Branching and Merging](#branching-and-merging)
5. [Remote Repositories](#remote-repositories)
6. [Stashing and Cleaning](#stashing-and-cleaning)
7. [Collaborating with GitHub](#collaborating-with-github)
8. [Advanced Git Topics](#advanced-git-topics)
9. [Git vs Github](#git-vs-github)
10. [Git Under The Hood](#git-under-the-hood)
11. [Git Hooks](#git-hooks)
12. [Resources](#resources)


## Introduction to Git

Git is a distributed version control system that helps you track changes in your code and collaborate with others, which was developed by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds). GitHub is a platform that hosts Git repositories, making it easier to share and manage code collaboratively. 

## Setting Up Git

### Installing Git
- **Linux**: `sudo apt-get install git`
- **Mac**: `brew install git`
- **Windows**: For windows please navigate to the donwloads page for [Git](https://git-scm.com/downloads) and download and execute the [Installer](https://git-scm.com/download/win), it will install the Git on you machine.

### Configuration
- Set your name: `git config --global user.name "Your Name"`
- Set your email: `git config --global user.email "your.email@example.com"`
- Check your settings: `git config --list`
- Check your user level settings: `git config --global --list`
- Check your system level settings: `git config --system --list`
- Check your single local repo level settings: `git config --local --list`

  
## Basic Git Commands

### Starting a Repository
- Initialize a new repository: `git init`
- Clone an existing repository: `git clone <repository-url>`

### Making Changes
- Check the status of your repository: `git status`
- Add files to staging: `git add <file>`
- Add all files to staging: `git add .` or `git add --all`
- Commit changes: `git commit -m "Your commit message"`
- View commit history: `git log`

### Viewing Changes
- Show changes in files: `git diff`
- Show changes between commits: `git diff <commit1> <commit2>`
- Show changes in the staging area: `git diff --staged`

## Branching and Merging

### Working with Branches
- List all branches: `git branch`
- Create a new branch: `git branch <branch-name>`
- Switch to a branch: `git checkout <branch-name>`
- Create and switch to a new branch: `git checkout -b <branch-name>`
- Delete a branch: `git branch -d <branch-name>`

![Git Workflow](https://i.redd.it/nm1w0gnf2zh11.png "a title")
### Merging
- Merge a branch into the current branch: `git merge <branch-name>`
- Abort a merge: `git merge --abort`
- Resolve merge conflicts manually, then add the resolved files: `git add <file>`, and commit.

## Remote Repositories

### Connecting to a Remote
- Add a remote repository: `git remote add origin <repository-url>`
- View remote repositories: `git remote -v`

### Pushing and Pulling
- Push changes to a remote repository: `git push origin <branch-name>`
- Pull changes from a remote repository: `git pull origin <branch-name>`

### Fetching
- Fetch changes from a remote repository: `git fetch origin`

## Stashing and Cleaning

### Stashing
- Stash changes: `git stash`
- List stashes: `git stash list`
- Apply a stash: `git stash apply`
- Apply and drop the stash: `git stash pop`
- Drop a stash: `git stash drop`

### Cleaning
- Remove untracked files: `git clean -f`
- Remove untracked directories: `git clean -fd`
- Perform a dry run to see what would be deleted: `git clean -n`

## Collaborating with GitHub

### Forking a Repository
1. Navigate to the repository on GitHub.
2. Click the "Fork" button at the top right.

### Cloning Your Fork
- Clone your forked repository: `git clone <forked-repo-url>`

### Creating a Pull Request
1. Make changes and commit them to your fork.
2. Push changes to your forked repository: `git push origin <branch-name>`
3. Navigate to the original repository on GitHub.
4. Click "New Pull Request" and follow the prompts.

## Advanced Git Topics

### Rebase
- Rebase current branch onto another branch: `git rebase <branch>`
- Abort a rebase: `git rebase --abort`
- Continue a rebase after resolving conflicts: `git rebase --continue`

### Rebase vs Merge 
![Merge vs Rebase](https://miro.medium.com/v2/resize:fit:1400/1*s9vhZ0Arc0ViAnl9ksy_Ew.png "a title")
### Cherry-picking
- Apply the changes from a specific commit: `git cherry-pick <commit>`

### Reverting and Resetting
- Revert a commit: `git revert <commit>`
- Reset to a previous commit: `git reset --hard <commit>`

## Git vs GitHub

| Feature            | Git                                                               | GitHub                                                                   |
|--------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------|
| **Type**           | Distributed Version Control System (Offline)                      | Web-based hosting service for Git repositories (Online)                  |
| **Functionality**  | Manages source code history and versioning locally and remotely   | Adds collaboration features, such as pull requests and issues            |
| **Installation**   | Installed on local machines                                       | Accessed via web browser, with additional tools available for desktop    |
| **Repository**     | Local and remote repositories                                     | Remote repositories hosted on GitHub's servers                           |
| **Branching**      | Supports branching and merging                                    | Provides visual tools for managing branches                              |
| **Collaboration**  | Primarily local, with push/pull to remote repositories            | Facilitates team collaboration, code reviews, and discussions            |
| **Access Control** | SSH keys, HTTPS, and GPG                                          | Granular access control and permissions                                  |
| **Integration**    | Works with various CI/CD tools                                    | Native integration with GitHub Actions, and third-party CI/CD tools      |
| **Community**      | Command-line focused community                                    | Large community with social coding features, such as following and stars |
| **Learning Curve** | Steeper learning curve due to command-line interface              | More accessible with a user-friendly interface                           |

---
## Git Under The Hood
The .git directory is a hidden folder that exists in the root of a Git repository. It contains all the metadata and information that Git needs to manage the version history of a project. Here’s a brief overview of its main components:

- Configuration Files (config):
Contains project-specific Git settings, such as remote repository URLs and branch information.

- Object Store (objects/):
Stores all the content tracked by Git in the form of objects, including commits, trees (directories), and blobs (files).

- References (refs/):
Tracks pointers to commit objects, such as branches, tags, and remote references.

- Index (index):
A staging area where changes are listed before they are committed to the repository. It acts as a snapshot of the working directory.

- Logs (logs/):
Contains a history of updates to the branches and references, allowing you to see how the repository has evolved over time.

- HEAD:
A special reference that points to the current branch or commit checked out in your working directory.

- Hooks (hooks/):
Contains scripts that can be triggered by specific Git events, such as commit, push, or merge. These scripts can automate tasks like code formatting or running tests.

- Packed References (packed-refs):
Stores a more compact representation of refs (branches, tags) when the number of references grows large.

## Git Hooks

Git hooks are scripts that Git executes before or after events such as commit, push, and receive. They allow you to automate tasks and enforce policies.There are client side and server side hooks.
Git Client Hooks vs Server Hooks

Git hooks are scripts that run automatically at specific points in the Git workflow. They can be used to enforce policies, validate data, and automate tasks. There are two types of Git hooks: client-side hooks and server-side hooks.

### Client-Side Hooks

Client-side hooks run on the developer's local machine, before the code is pushed to the remote repository. These hooks are stored in the .git/hooks directory of the local repository.

Advantages:

Flexibility: Client-side hooks can be customized to fit individual developer needs.
Performance: Since they run locally, client-side hooks don't impact the performance of the remote repository.
Security: Client-side hooks can help prevent sensitive data from being committed to the repository.
Disadvantages:

Lack of enforcement: Client-side hooks can be bypassed or disabled by developers.
Inconsistency: Different developers may have different client-side hooks, leading to inconsistencies.
Server-Side Hooks

Server-side hooks run on the remote repository, after the code has been pushed. These hooks are stored in the hooks directory of the remote repository.

Advantages:

Enforcement: Server-side hooks are enforced for all developers, ensuring consistency and compliance.
Centralized management: Server-side hooks can be managed centrally, making it easier to maintain and update.
Security: Server-side hooks can help prevent unauthorized changes to the repository.
Disadvantages:

Performance impact: Server-side hooks can impact the performance of the remote repository.
Limited flexibility: Server-side hooks are less flexible than client-side hooks, as they need to be compatible with all developers' environments.
Common Use Cases:

### Client-Side Hooks:

Code formatting: Enforce code formatting standards before committing code.
Commit message validation: Validate commit messages to ensure they meet specific requirements.
Sensitive data detection: Detect and prevent sensitive data from being committed to the repository.
Server-Side Hooks:

Access control: Enforce access control policies, such as restricting pushes to specific branches or users.
Code review: Enforce code review policies, such as requiring approvals before merging code.
Data validation: Validate data before accepting it into the repository.
In summary, client-side hooks are useful for enforcing individual developer policies and detecting sensitive data, while server-side hooks are better suited for enforcing centralized policies, access control, and data validation.

## Resources
- [Official Git Documentation](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git and Github Mastery Video Tutorial](https://www.youtube.com/watch?v=zTjRZNkhiEU)
- [Git Internals](https://www.youtube.com/watch?v=fWMKue-WBok&list=PL9lx0DXCC4BNUby5H58y6s2TQVLadV8v7)

---

This cheat sheet is for everyone be it beginner or a seasoned professional, who want to learn git or master git concepts, more updations will be added and we're expecting collaboration from other computer science enthusiasts. 
