# Git Workflow Examples & Sample Scenarios

This directory contains real-world Git workflows and example use cases to help practice version control beyond basic commands. Each section includes steps, expected outcomes, and recommended exercises.

---

## Example 1: Basic Local Workflow

```
git init
echo "Hello Git" > file.txt
git add file.txt
git commit -m "Initial commit"
```

Outcome:
Local Git repository created with first version tracked.

---

## Example 2: Create Feature Branch & Merge

```
git checkout -b feature-login
# Make code changes
git add .
git commit -m "Added login feature"
git checkout main
git merge feature-login
```

Outcome:
Feature branch development completed and merged into main.

---

## Example 3: GitHub Remote Setup

```
git remote add origin <repo-url>
git push -u origin main
```

Outcome:
Local repository connected to GitHub and pushed remotely.

---

## Example 4: Pull, Fetch & Sync

```
git pull origin main       # Download + merge
git fetch origin           # Download only
git merge origin/main      # Merge manually if needed
```

Outcome:
Local repo updated with remote changes.

---

## Example 5: Handling Merge Conflict

1. Create two branches modifying the same line:

```
git checkout -b fix-version
git checkout -b ui-change
```

2. Modify file differently in both branches and merge.
3. Git will throw a conflict.
4. Resolve manually and commit.

Outcome:
Understanding of conflict resolution and team scenario handling.

---

## Example 6: Rebase Instead of Merge

```
git checkout feature-1
git rebase main
```

Outcome:
Cleaner commit history with linear progress.

---

## Example 7: Using Stash for Quick Save

```
git stash
git switch main
git stash apply
```

Outcome:
Uncommitted work temporarily saved and restored.

---

## Example 8: Tag & Release Example

```
git tag v1.0
git push origin v1.0
```

Outcome:
First stable release version created.

---

## Example 9: Cherry Pick Commit

```
git checkout hotfix
git cherry-pick <commit-id>
```

Outcome:
Specific commit copied from one branch to another.

---

## Example 10: Full Real-World Workflow

```
git clone <repo>
git checkout -b feature-api
git add .
git commit -m "API logic added"
git push origin feature-api
# Create Pull Request on GitHub
git merge feature-api
git branch -d feature-api
```

Outcome:
End-to-end development cycle replicated.

---

### Recommended Practice Projects

| Project   | Scenario                               |
| --------- | -------------------------------------- |
| Project A | Feature creation + merge workflow      |
| Project B | Conflict resolution testing            |
| Project C | Rebase + linear history maintenance    |
| Project D | Cherry-pick controlled commit movement |
| Project E | Tag-based release management           |

---

