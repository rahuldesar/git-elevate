git diff
git rebase
git tag

### git remote

- Manage set of tracked repositories
- BETTER CHECK `git help remote`

```
//Learn Later
git remote
git remote add                             ==> FOR DESCRIPTIONS . better check `git help remote`
git remote rename
git remote remove
git remote set-head
git remote set-branches
git remote get-url
git remote set-url
git remote get-url --add
git remote set-url --delete
git remote show

```

### git reset

- Resets changes in the staging area or working directory.

```
git reset HEAD <file>                  ==> Unstage changes for a specific file.
git reset --soft HEAD                  ==> Undo the last commit, keeping the changes staged.
git reset --mixed HEAD                 ==> Undo the last commit and unstage the changes.
git reset --hard HEAD                  ==> Undo the last commit and delete the changes.
git reset --hard HEAD                  ==> Discard all local changes and reset to the last commit.
git reset <commit>                     ==> Reset to a specific commit, discarding any commits after it.
git reset --hard origin/master         ==> Reset to the latest version of the remote master branch.

```

### git stash

- Stashes changes in a temporary area.

```
git stash push
git stash save
git stash list
git stash show
git stash pop
git stash apply
git stash branch
git stash clear
git stash drop
git stash create
git stash store
```
