# Git Lab 5 – Tags & Releases

## Commands I Learned
- `git tag v1.0` → create a lightweight tag for the current commit.
- `git tag -a v1.0 -m "message"` → create an annotated tag with a description.
- `git tag` → list all tags in the repository.
- `git show v1.0` → show details of the commit marked by the tag.
- `git push origin v1.0` → push a specific tag to the remote.
- `git push origin --tags` → push all local tags to the remote.
- `git tag -d v1.0` → delete a tag locally.
- `git push origin --delete v1.0` → delete a tag from the remote.

## My Understanding
- Tags are like **sticky notes** on specific commits — they don’t move like branches.
- Lightweight tags are simple pointers; annotated tags include metadata (author, date, message).
- Tags are commonly used to mark **release versions** (v1.0, v2.0, etc.).
- Once pushed, tags can be turned into **GitHub Releases** with notes and files.
- Releases help teams and users know exactly which version is stable and ready.

## Key Learning
- Tags = version markers in Git history.
- Releases = official announcements of those versions.
- Together, they make collaboration, deployment, and rollback much easier.

