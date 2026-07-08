# Git Lab 4 – Pull Requests

## Commands I learned
- git branch → create a new branch
- git checkout → switch to a branch
- git checkout -b → create and switch in one step
- git push origin branch-name → push branch to GitHub
- Pull Request → propose changes from branch to master

## My Understanding
Pull Requests are the standard way to merge code in collaborative projects.  
They allow team members to review, comment, and approve changes before merging into the master branch.  
When a branch is pushed to GitHub, I can open a Pull Request to integrate those changes.  
If commits are made in master before creating a branch, the branch will include them.  
If commits are made in master after the branch is created, the branch won’t see them unless I merge or rebase.

## Key Learning
- Branches are snapshots of master at the time of creation.  
- Always pull remote changes before pushing to avoid rejection errors.  
- Use Pull Requests for clean, collaborative merges instead of merging only locally.

