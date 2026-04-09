# Initialize, Commit, and Branch Basics

# Objective
- Initialize a new Git repository.
- Create a few files and commit them.
- Create a new branch, make changes, and merge it back to the main branch.

## Step 1 : Initialize a new Git repository
```bash
git init
```

## Step 2 : Create a few files and commit them
```bash
touch example.py
```
- Add some content to `example.py`

## Step 3 : Stage and commit the changes
```bash
git add example.py
git commit -m "Files added"
```

## Step 4 : Create a new branch
```bash
git checkout -b newbranch
```

## Step 5 : Create a new file and commit it
```bash
touch example1.py
git add example1.py
git commit -m "changes made in new branch"
``` 

## Step 6 : Merge the new branch back to the master branch
```bash
git checkout master
git merge newbranch
```
## Step 7 : Check the status of the repository
```bash
git status
git log
```