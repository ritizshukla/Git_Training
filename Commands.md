# 🚀 Git Commands Reference

A complete reference guide of frequently used Git commands with short explanations and examples.

---

## 1. Setup and Configuration

| Operation    | Command                                            | Description                      |
| ------------ | -------------------------------------------------- | -------------------------------- |
| Set username | `git config --global user.name "Your Name"`        | Sets global username for commits |
| Set email    | `git config --global user.email "you@example.com"` | Sets global user email           |
| View config  | `git config --list`                                | Displays configuration details   |

---

## 2. Creating and Initializing

| Operation       | Example           | Notes                                           |
| --------------- | ----------------- | ----------------------------------------------- |
| Initialize repo | `git init`        | Convert folder to a Git repository              |
| Clone repo      | `git clone <url>` | Create a copy of a remote repo on local machine |

---

## 3. Stage, Commit & Modify

| Action              | Command                   |
| ------------------- | ------------------------- |
| Stage files         | `git add <file>`          |
| Stage all files     | `git add .`               |
| Commit with message | `git commit -m "message"` |
| Amend last commit   | `git commit --amend`      |

---

## 4. Branching & Working with Branches

| Action                 | Command                    |
| ---------------------- | -------------------------- |
| Create branch          | `git branch <name>`        |
| Switch branch          | `git checkout <branch>`    |
| Create & switch branch | `git checkout -b <branch>` |
| List branches          | `git branch -a`            |
| Delete branch          | `git branch -d <branch>`   |

---

## 5. Remote Repositories

| Action               | Command                       |
| -------------------- | ----------------------------- |
| Add remote           | `git remote add origin <url>` |
| View remote          | `git remote -v`               |
| Push to remote       | `git push origin <branch>`    |
| Pull updates         | `git pull`                    |
| Fetch remote changes | `git fetch`                   |

---

## 6. Merge & Rebase

| Action          | Command                 |
| --------------- | ----------------------- |
| Merge branch    | `git merge <branch>`    |
| Start rebase    | `git rebase <branch>`   |
| Abort rebase    | `git rebase --abort`    |
| Continue rebase | `git rebase --continue` |

---

## 7. Logs & History

| Action              | Command                           |
| ------------------- | --------------------------------- |
| View commit history | `git log`                         |
| One-line log        | `git log --oneline`               |
| Graph view          | `git log --oneline --graph --all` |
| Show diff           | `git diff`                        |

---

## 8. Undo & Restore

| Action            | Command                        |
| ----------------- | ------------------------------ |
| Undo staged files | `git restore --staged <file>`  |
| Restore file      | `git restore <file>`           |
| Reset to commit   | `git reset --hard <commit-id>` |

---

## 9. Stash

| Action           | Command           |
| ---------------- | ----------------- |
| Stash changes    | `git stash`       |
| Show list        | `git stash list`  |
| Apply last stash | `git stash apply` |
| Drop last stash  | `git stash drop`  |

---

## 10. Linking Local Repo ↔ GitHub

### Push Local Project to GitHub (First Time)

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main
```

---

### Connect Existing GitHub Repo

```bash
git clone <repo-url>
cd <repo-name>
```

---

### Push Changes

```bash
git add .
git commit -m "message"
git push
```

---

### Pull Updates

```bash
git pull origin main
```

---

### Change Remote URL

```bash
git remote set-url origin <new-url>
```

---

### Remove Remote

```bash
git remote remove origin
```

---

## 11. SSH Setup

### Generate SSH Key
```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

### Start SSH Agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Copy Key
```bash
cat ~/.ssh/id_ed25519.pub
```

### Test Connection
```bash
ssh -T git@github.com
```

---

## 12. Typical Workflow

```bash
git pull
git add .
git commit -m "feat: update project"
git push
```

---

## 13. Advanced (Future)

- Cherry-pick
- Interactive rebase
- Git hooks
- Tagging
- Submodules
