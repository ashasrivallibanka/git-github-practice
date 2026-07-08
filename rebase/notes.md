# Git Lab 5 – Rebase & Conflicts

## Commands I Learned
- `git rebase master` → replay feature branch commits on top of master.
- `git rebase --continue` → continue rebase after resolving conflicts.
- `git add <file>` → mark conflict file as resolved.
- `git merge feature-branch` → merge feature branch into master.
- `git push --force origin branch-name` → push rebased branch to GitHub.
- `git pull --rebase origin master` → update local master with remote changes before pushing.

## My Understanding
- Rebase rewrites history so feature branch commits appear after master’s latest commits.
- Conflicts occur when both master and feature branch edit the same file differently.
- Git shows conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) and pauses until resolved.
- After resolving, rebase continues and history becomes linear.
- Merge is still needed at the end to bring feature branch changes into master.
- If local and remote master diverge, Git blocks push to prevent overwriting.  
  - Fix by pulling with rebase or force pushing if local history should replace remote.

## Key Learning
- **Rebase** → clean, linear history (no merge commits).
- **Merge** → combines histories, may add a merge commit.
- **Conflict resolution** → edit file manually, then `git add` and `git rebase --continue`.
- Always push with `--force` after rebase since history changes.
- Use `git pull --rebase` before pushing to avoid rejection errors when remote has new commits.

## ASCII Diagram

### Without Rebase (merge commit added)
Master: A --- D
             \
Feature:      B --- C
               \
                Merge Commit (M)

- Master had commit **D**.
- Feature branch had commits **B, C**.
- Git joined them with a special **merge commit (M)**.
- History looks like a fork that joins back together.

### With Rebase (clean linear history)
Master: A --- D --- B --- C

- Master had commit **D**.
- Feature branch commits **B, C** were replayed after D.
- History is straight, no fork, no merge commit.

## Easy Analogy
- **Merge** → stapling two notebooks together (you see the staple = merge commit).
- **Rebase** → copying feature pages and pasting them neatly after master’s pages (no staple, clean story).
- **Conflict** → two kids draw on the same page differently; you decide how to fix it.

## Summary
- Rebase cleans history, Merge delivers the work into master.
- Merge creates one more new commit, Rebase rewrites with latest master.
- Conflicts are normal when both branches edit the same file.
- Push divergence errors happen when local and remote histories differ — fix with pull + rebase or force push.

