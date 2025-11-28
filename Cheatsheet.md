# Ultimate Git Quick Revision Cheatsheet

## Setup (One-Time)

```
git config --global user.name "Name"
git config --global user.email "mail@example.com"
git config --list
```

---

## Core Workflow (4-Step)

```
1. git status
2. git add <file> / git add .
3. git commit -m "message"
4. git push origin <branch>
```

---

## Create / Clone / Init

```
git init                # Start repo
git clone <url>         # Copy remote repo to local
```

---

## Branching: 90% of Git Use

```
git branch              # List
git branch <name>       # Create
git checkout <name>     # Switch
git checkout -b <name>  # Create + switch
git merge <branch>      # Merge into current
git branch -d <name>    # Delete
```

---

## Remote & Push/Pull

```
git remote -v
git remote add origin <url>
git push -u origin <branch>   # First push
git pull                      # Get latest (pull = fetch + merge)
git fetch                     # Only downloads changes
```

---

## Logs & History (Revision Critical)

```
git log --oneline --graph --all
git diff                      # Show unstaged changes
git diff --staged             # Show staged changes
```

---

## Undo / Restore / Reset (High-Value)

```
git restore <file>              # Undo working copy changes
git restore --staged <file>     # Remove from staging
git reset --soft <commit>       # Keep changes staged
git reset --hard <commit>       # Full rollback (Dangerous!)
```

---

## Stash (Underrated)

```
git stash
git stash list
git stash apply
git stash drop
```

---

## Tags (Deployment & Releases)

```
git tag <tagname>
git push origin <tagname>
```

---

### If you only remember 10 commands:

```
git status
git add .
git commit -m "msg"
git push
git pull
git branch
git checkout -b <branch>
git merge <branch>
git log --oneline
git stash
```

