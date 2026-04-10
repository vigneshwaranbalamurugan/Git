# Stashing Changes for Context Switching
# Objective
- Learn how to use Git stash to save uncommitted work temporarily.

# Steps
1. Create a new file named `example.py` and add some content to it.
```python
Hello world.
```
2. Use Git stash to save changes without committing them.
```bash
git stash
```
3. Change the branch.
```bash
git checkout -b stash-branch
```
4. Make some changes in the new branch.
```python
Hello World.
This is a new branch.
```
5. Now, switch back to the original branch.
```bash
git checkout master
```
6. Reapply stashed changes.
```bash
git stash pop
```
```python
Hello world.
```
7. List all stashes
```bash
git stash list
```
8. Drop specific stash
```bash
git stash drop "stash@{0}
```
