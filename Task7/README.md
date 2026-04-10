# Cherry-Picking Commits Between Branches
# Objective:
- Selectively apply a commit from one branch to another using cherry-
pick.

# Code
```bash
git checkout cherry1
git add .
git commit -m "cherry1"

git checkout cherry2
git add .
git commit -m "cherry2"

git log --oneline

git checkout cherry1
git cherry-pick 048cf6f
```
