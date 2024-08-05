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
9. [Resources](#resources)

## Introduction to Git

Git is a distributed version control system that helps you track changes in your code and collaborate with others, which was developed by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds). GitHub is a platform that hosts Git repositories, making it easier to share and manage code collaboratively. 

## Setting Up Git

### Installing Git
- **Linux**: `sudo apt-get install git`
- **Mac**: `brew install git`
- **Windows**: Download and install from [git-scm.com](https://git-scm.com/)

### Configuration
- Set your name: `git config --global user.name "Your Name"`
- Set your email: `git config --global user.email "your.email@example.com"`
- Check your settings: `git config --list`

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

### Cherry-picking
- Apply the changes from a specific commit: `git cherry-pick <commit>`

### Reverting and Resetting
- Revert a commit: `git revert <commit>`
- Reset to a previous commit: `git reset --hard <commit>`

## Resources
- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git and Github Mastery Video Tutorial](https://www.youtube.com/watch?v=zTjRZNkhiEU)

---

This cheatsheet is designed to be a quick reference guide to help you on your journey to mastering Git and GitHub. Happy coding!
