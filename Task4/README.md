# Simulating and Resolving Merge Conflicts

# Objective:
- Create a scenario that produces a merge conflict and resolve it.

## Step 1: Create a Merge Conflict
1. Create a new branch from the master branch:
```bash
git checkout -b branch1
```
2. Make changes to a example.py and commit the changes:
```bash
print("Hello World 1")
```
```bash
git add .
git commit -m "Branch 1 commit"
```
3. Switch back to the master branch and create another branch:
```bash
git checkout master
git checkout -b branch2
```
4. Make different changes to the same example.py file and commit the changes:
```bash
print("Hello World 2")
```
```bash
git add .
git commit -m "Branch 2 commit"
```
5. Now, try to merge branch1 into branch2:
```bash
git checkout branch2
git merge branch1
```
This will result in a merge conflict because both branches have made changes to the same line in example.py.
```bash
Auto-merging Task4/example.py
CONFLICT (content): Merge conflict in Task4/example.py
Automatic merge failed; fix conflicts and then commit the result.
```
## Step 2: Resolve the Merge Conflict
1. Open the example.py file in a text editor.
```bash
<<<<<<< HEAD
print("Hello World 2")
========
print("Hello World 1")
>>>>>>>branch1
```
2. Edit the file to resolve the conflict. 
```bash
print("Hello World 1")
print("Hello World 2")
```

3. Commit the resolved conflict
```bash
git add .
git commit -m "Resolved conflict"
```