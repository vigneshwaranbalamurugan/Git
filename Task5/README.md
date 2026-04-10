# Interactive Rebasing for Clean Commit History

# Objective:
- Use interactive rebase to tidy up your commit history

# Steps:
1. Create a file named example.txt and add some content to it.
2. Make several commits with different messages to simulate a messy commit history.
```bash
Hello world
```
```bash
git add .
git commit -m "Initial commit"
```
```bash
Hello World.
Minor change.
```
```bash
git add .
git commit -m "minor change"
```
```bash
Hello World.
Minor change.
Typo error.
```
```bash
git add .
git commit -m "typo eror"
```
```bash
Hello World.
Minor change.
Typo error
Major change.
```
```bash
git add .
git commit -m "major change"
```
3. Git rebase and Squash commits:
```bash
git rebase -i HEAD~4
```
```bash
pick a1b2c3 initial commit
pick d4e5f6 minor change
pick g7h8i9 typo eror
pick j1k2l3 minor change
```
- change the third commit to reword and the fourth commit to squash:
```bash
pick a1b2c3 initial commit
pick d4e5f6 minor change
reword g7h8i9 typo error
squash j1k2l3 major change
```
4. Save and close editor.
