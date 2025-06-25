# Git Stuff

##### Made this just incase i forgor

## 🔧 Basic Setup

```bash
git init                  # Initialize a new Git repository
git config --list         # Show current Git configuration
```

---

## 📄 Working Directory & Staging

```bash
git status                # Show status of working directory
git add <file>            # Stage changes for commit
git rm <file>             # Remove file and stage the removal
```

---

## ✅ Commit History

```bash
git commit -m "msg"                          # Commit staged changes with message
git log                                      # Show commit history
git log -- <file>                            # Show commits affecting a specific file
git log --all --decorate --oneline --graph   # Visualize all branches in one line
```

---

## 🌿 Branching & Merging

### Branch Management

```bash
git branch                # List all local branches
git branch -d <branch>    # Delete a branch
git branch --merged       # Show merged branches
```

### Switching & Checkout

```bash
git checkout <branch>               # Switch to a branch
git checkout <commit> -- <file>     # Restore a file from specific commit
```

### Merging

```bash
git merge <branch>        # Merge a branch into current branch
git rebase <branch>       # Reapply commits on top of another base branch
```

### Merge Types

**Fast-forward Merge** (no new commits, pointer just moves forward):

```
Before:
A---B---C (feature)
    ↑
    main

After:
A---B---C (main, feature)
```

**Three-way Merge** (creates a new merge commit):

```
Before:

     D---E (feature)
    /
A---B---C (main)

After:
     D----E (feature)
    /      \
A---B---C---M (main)
            ↑
        Merge commit
```

---

## 🌐 Remote Repositories

### Managing Remotes

```bash
git remote                   # List remote connections
git remote -v                # Show remote URLs
git remote add <name> <url>  # Add a new remote
```

### Fetching & Pulling

```bash
git clone <url>              # Clone a repository
git fetch                    # Fetch from default remote
git fetch <remote>           # Fetch from specific remote
git pull                     # Fetch and merge from default remote
git merge <remote>/<branch>  # Merge specific remote branch
```

### Pushing Changes

```bash
git push                           # Push local commits to remote
git push origin --delete <branch>  # Delete a remote branch
```
