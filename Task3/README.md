# Undoing Changes and Reverting Commits

# Objective:
- Experiment with undoing changes in your working directory and
commits.

## Step 1: Create and commit a file

- Create a file:

```bash
touch file.txt
```

Add content:

Hello Git

- Stage and commit:
```bash
git add file.txt
git commit -m "Initial commit"
```
## Step 2: Modify a tracked file and undo changes

- Modify the file:
Hello World

- Check status:

```bash 
git status 
```

- Undo changes using:
```bash
git restore file.txt
```

- File returns to last committed version
- Changes removed from working directory

## Step 4: Undo commit safely using git revert
```bash
git revert HEAD
```
- Creates a new commit
- Reverses changes from previous commit
- Keeps history safe

## Step 5: Undo commit using git reset

- Remove last commit (keep changes staged):

```bash 
git reset --soft HEAD~1
```

- Commit removed
- Changes still staged

- Remove last commit (keep changes in working directory):
```bash
git reset HEAD~1
```
- Commit removed
- Changes still present but unstaged

- Remove last commit permanently
```bash
git reset --hard HEAD~1
```
- Commit removed
- Changes deleted permanently
