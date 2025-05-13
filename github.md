# Git Collaboration Guide

## Key Components

1. **Single Source of Truth (Remote Server)**
   * Central repository hosted on platforms like GitHub, GitLab, or BitBucket
   * Serves as the authoritative version of the codebase

2. **Developer Workstations**
   * Local environments where developers make changes
   * Each developer has their own local copy of the repository

3. **Git Operations**
   * **Push**: Send local commits to the remote repository
   * **Pull**: Fetch changes from the remote repository and integrate them into local copy

## GitHub Integration Commands

### Connecting to Remote Repository

Connect your local repository to GitHub:

```bash
# Add remote repository with the name "origin"
git remote add origin git@github.com:username/repository.git

# Verify remote connections
git remote -v
```

### Branch Naming

Update your branch name from the default "master" to "main":

```bash
# Rename branch from master to main
git branch -M main
```

### Synchronizing with Remote

Always pull before pushing to avoid conflicts:

```bash
# Pull remote changes with rebase
git pull --rebase origin main
```

> **Note about rebase**: Using `--rebase` ensures your local commits are applied on top of the latest remote changes, creating a cleaner commit history.

### Pushing to Remote

Push your local changes to the remote repository:

```bash
# Push to remote and set upstream tracking
git push -u origin main
```

> The `-u` (or `--set-upstream`) flag sets the remote branch as the upstream branch for your local branch, so you can use `git pull` and `git push` without additional parameters in the future.

## Best Practices for Collaboration

1. **Always pull before pushing** to ensure you have the latest changes
2. **Use descriptive commit messages** to make the history understandable
3. **Create feature branches** for new work instead of working directly on main
4. **Regularly sync with the remote repository** to minimize merge conflicts
5. **Use meaningful branch names** that describe the feature or fix

## Common Workflow for New Features

```bash
# Make changes and commit them
git add .
git commit -m "Descriptive message about the changes"

# Pull latest changes from main branch
git checkout main
git pull

# Return to feature branch and rebase onto main
git checkout feature-name
git rebase main

# Push feature branch to remote
git push -u origin feature-name

# Create pull request on GitHub
# After approval, merge into main branch
```
