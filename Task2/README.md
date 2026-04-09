# Using .gitignore and Tracking Files

# Objective
- Set up a .gitignore file to exclude certain files or directories.
- Verify that ignored files are not tracked by Git.

## Step 1 : Create a .gitignore file
```bash
touch .gitignore
```
- Open the .gitignore file and add .env:
```
.env
```
## Step 2 : Create a tracked file and an untracked file
```bash
touch example.py
touch .env
```
- Add some content to `example.py` and `.env`

## Step 3 : Stage and commit the tracked file
```bash
git add .
git commit -m "Gitignore"
```

## Step 4 : Check the status of the repository
```bash
git status --ignored
```

``` On branch master
Your branch is up to date with 'origin/master'.

Ignored files:
  (use "git add -f <file>..." to include in what will be committed)
        .env

nothing to commit, working tree clean
```