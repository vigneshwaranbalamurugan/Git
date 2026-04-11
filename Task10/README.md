# Comprehensive Workflow with Forced Pushes and Recovery

# Requirements:
- Simulate an advanced Git scenario that includes forced pushes,
recovering lost commits, and a multi-branch workflow.
- Create a repository with multiple branches representing features, bug
fixes, and releases.
- Simulate a scenario where a forced push ( git push --force ) is required
(for example, after rewriting history with an interactive rebase).
- Use git reflog to locate and recover lost commits after a mistaken
force push.
- Document each step, explaining how and why forced pushes should
be handled with care, and how git reflog can be a lifesaver.
- Discuss best practices for collaborating with teams when rewriting
history and using force pushes.

# Steps
```bash
git checkout -b main
git add README.md
git commit -m "Initial commit"
git checkout -b feature-login
git add login.txt
git commit -m "Added login"
update login.txt
git add login.txt
git commit -m "Updated login"
git checkout main
git checkout -b bugfix-header
git add header.txt
git commit -m "Added header"
git checkout main
git checkout -b release-v1
git push -u origin main
git push -u origin feature-login
git push -u origin bugfix-header
git push -u origin release-v1
git checkout feature-login
git rebase -i HEAD~2
Update the commit messages and squash commits.
git push origin feature-login --force
git reflog
git checkout HEAD@{1}
git branch -b recovered-branch
```