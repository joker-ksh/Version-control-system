# Git Cheat Sheet

## 🔧 Git Configuration

**Set global Git user name:**
```bash
git config --global user.name "<name>"
```

**Get current global Git user name:**
```bash
git config --global user.name
```

**Set global Git email:**
```bash
git config --global user.email "<email>"
```

**Get current global Git email:**
```bash
git config --global user.email
```

## 📁 Repository Initialization

**Initialize a new Git repository in the current directory:**
```bash
git init
```

## 📥 Adding & Removing Files

**Add a specific file to the staging area:**
```bash
git add <file path>
```

**Add all files to the staging area:**
```bash
git add .
```

**Remove a file from Git and the file system:**
```bash
git rm <file path>
```

## 🔍 Viewing Changes

**View unstaged changes (differences between working directory and index):**
```bash
git diff
```

**Check the status of your working directory and staging area:**
```bash
git status
```

## ✅ Committing Changes

**Commit staged changes with a message:**
```bash
git commit -m "your commit message"
```

## 🕒 Viewing Commit History

**Show complete commit logs:**
```bash
git log
```

**Show commit logs in a single-line format:**
```bash
git log --oneline
```

## ♻️ Undoing Commits

**Reset to a specific commit and remove all changes after it (destructive):**
```bash
git reset --hard <commit ID>
```

**Revert a specific commit (non-destructive):**
```bash
git revert <commit ID>
```

## 🧠 Git Internals Concept

Commits in Git form a linked list. Each commit stores a snapshot of the code. The HEAD points to the most recent commit.

```
(commit A) ← (commit B) ← (commit C) ← HEAD
```

## 🧭 Git Workflow Diagram

This diagram shows how changes move through Git:

```
Working Directory → Staging Area → Commit History
```

Commands involved:
- `git add`
- `git commit`
- `git diff`
- `git reset`
- `git revert`

## 📌 Summary Table

| Command | Description |
|---------|-------------|
| `git init` | Initialize a Git repository |
| `git add <file>` | Add file to staging |
| `git add .` | Add all files to staging |
| `git diff` | View unstaged changes |
| `git commit -m "msg"` | Commit staged files |
| `git status` | Show status of staging/working area |
| `git log` | View commit history |
| `git log --oneline` | Compact commit history |
| `git rm <file>` | Remove file from Git |
| `git reset --hard <id>` | Reset to a specific commit (destructive) |
| `git revert <id>` | Revert a commit safely |
