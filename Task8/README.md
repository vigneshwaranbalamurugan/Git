# Using Git Hooks for Automated Checks
# Objective
- Set up a Git hook to run scripts (like linters or tests) before commits are finalized.

# Steps:
1. Navigate to `.git/hooks`
2. Create new file named `pre-commit`
3. Add this to the file:
```bash
#!/bin/sh
echo "Running pre-commit checks..."
if git diff --cached | grep -i "TODO"
then
    echo "Commit blocked: Remove TODO comments before committing."
    exit 1
fi

echo "Pre-commit checks passed!"
exit 0
```
4. Save and make the file executable:
```bash
chmod +x pre-commit
```
5. try to commit
```bash
Running pre-commit checks...
-TODo
-TODO
❌ Commit blocked: Remove TODO comments before committing.
```