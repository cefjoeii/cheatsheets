---
title: Git
---

### Config

```
# Change commit author's name and email globally
  git config --global user.name "John Doe"
  git config --global user.email "john@doe.org"

# Change commit author's name and email per repository
  git config user.name "John Doe"
  git config user.email "john@doe.org"
```

### Clone

```
# Clone a repo with master branch as default
  git clone <url>

# Switch to another branch from remote after fresh clone
  git checkout -b <branch-name> <remote-name>/<branch-name>
  
# Clone a repo with the specific branch directly
  git clone -b <branch-name> <url>
```

### Remote

```
# View remote
  git remote -v

# Add a remote 
  git remote add <remote-name> <url>

# Edit a remote url
  git remote set-url <remote-name> <url>

# Delete a remote
  git remote rm <remote-name>
```

### Branch

```
# Create a new branch
  git checkout -b <branch-name>

# Push new branch to remote
  git push <remote-name> <branch-name> --set-upstream
  OR
  git push -u <remote-name> <branch-name>

# Rename a branch
  git branch -m <new-branch-name>

# Rename a branch when you're in a different branch
  git branch -m <old-branch-name> <new-branch-name>

# Delete the <old-branch-name> remote branch and push the <new-branch-name> local branch
  git push <remote-name><space>:<branch-name> <new-branch-name>

# Reset the upstream branch for the <new-branch-name> local branch
  git push <remote-name> -u <new-branch-name>

# Delete a branch
  git branch -d <branch-name>

# Delete a branch from remote
  git push <remote-name><space>:<branch-name>

# Fetch a branch from remote
  git fetch <remote-name>
  git checkout --track <remote-name>/<branch-name>
```

### Fetch, Pull, Merge

```
# Fetch all from tracked remotes/branches
  git fetch --all

# Pull and merge to current branch
  git pull <remote-name> <branch-name>

# Pull and resolve merge conflicts in favor of theirs
  git pull -X theirs <remote-name> <branch-name>

# Abort merge state due to conflict
  git merge --abort
```

### Commit

```
# View commit history
  git log

# View changes
  git status

# Add to staging area by file
  git add <file-name>

# Add all new, modified, and deleted files to staging area
  git add -A
  OR
  git add --all
  OR (Git Version 2.x)
  git add .
  
# Commit changes
  git commit -m "A descriptive but brief commit message"

# Add all and commit at the same time
  git commit -am "A descriptive but brief commit message"

# Edit last commit message
  git commit --amend -m "A new message"

# Edit last commit message with additional changes
  git add <stuff>
  git commit --amend -m "A new message with additional changes"

# Undo last commit and keep changes
  git reset HEAD

# Undo and go back to a specific commit
  git reset <commit-id>

# Undo last commit and discard changes
  git reset --hard HEAD
```

### Tag/Release

```
# Create a new tag
  git tag <tag-name>
  git push <remote-name> --tags

# Delete a tag
  git tag --delete <tag-name>
  git push --delete <remote-name> <tag-name>

# Or delete by pushing an empty reference to the remote tag name:
  git push <remote-name> :<tag-name>
```

### Delete Commit History
Warning: This is not recommended. Make sure you know what you’re doing.

```
# Checkout
  git checkout --orphan <new-branch-name>

# Add all the files
  git add -A

# Commit the changes
  git commit -m "Initial commit"

# Delete the branch
  git branch -D master

# Rename <new-branch-name> to master
  git branch -m master

# Force update your repository
  git push -f origin master

# Good house-keeping
  git gc --aggressive --prune=all
```
