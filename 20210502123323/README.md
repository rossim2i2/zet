# Github New Repo Cheat Sheet

## Creating a new GO project

1. CD to ~/repos/github.com/rossim2i2
2. Create a new repo: gh repo create {name of repo}
3. CD into new folder
4. Create new branch: branch initial
5. Create a new file: README.md
  • Vim - Add header
  • Type: gobadges github.com/rossim2i2/{name of repo}
  • Normal Mode Type: !!bash
  • Add body
  • Write and quit
6. Add new module: go mod init github.com/rossim2i2/{name of repo}
7. Add first file (Touch)
• Command: main.go
• Library: lib.go
8. Add changes to repo: add .
9. Check git stats: status
10. Commit changes: commit
• Give a commit message
11. Branch to main: branch main
12. Check branches: branches
13. Switch to main: switch main
14. Delete the initial branch: git branch -d initial
15. Check status to ensure everything is up to date: status
16. Push changes: git push -u origin main

## Notes

When working on changes, create a new branch to work on and commit
changes to. When ready to push the changes (after commit), use the
“merge” command. I.E. merge {branch name}.

This sub-function will automatically switch to the main branch, merge
the branch changes were made on, push the changes to github and delete
the old branch as it is no longer required.

Changes to code should always be done on another branch to ensure the
codebase on the main branch is not compromised.
