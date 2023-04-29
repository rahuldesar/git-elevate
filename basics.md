# GIT BASICS

**THIS DOESNOT COVER ALL GIT COMMANDS AND FLAGS.**

To list all available commands or additional help. Check:

```
 man git || git --help || git help -a || git help -g || git help <concept|command>
```

To checkout details about each command use:

```
man git-<command> || git help <command>
// man git-commit || git help commit
```

This is tailored to my own progress, and you might find this helpful.

---

### git init

- Initializes a new Git repository.

```
--template=<template_directory>
```

### git clone

- Clones an existing Git repository.

```
-l | --local            ==> repo is on local machine
-b | --branch <name>    ==> points cloned repo's head to <name> branch

// Learn Later
--depth <depth>
--shallow-since=<date>
--no-tags
```

### git add

- Adds changes to the staging area.

```
.                     ==> Add all changes to staging area
-A | --all            ==> Add all changes to staging area
-p | --patch          ==> selectively add changes within a file to staging area

// Learn Later
-u | --update         ==> updates the index with changes of tracked files.
```

### git status

- Shows the status of the working directory and staging area.

### git commit

- Commits changes to the local repository.

```
-m <msg> | --message=<msg>
-a | --all                ==> Automatically stages and commits any changes to tracked files.
--branch                  ==> Show the branch and tracking info even is short-format.
-F <file> | --file=<file> ==> take commit message from given file
-p | --patch              ==> interactive patch selection interface to choose which changes to commit.
-amend                    ==> Replaces the tip of current branch by creating a new commit
-v
-c <commit>

// Learn Later
-t <file> | --template=<file> ==> start the editor with the content in given file
--squash=<commit>
```

### git log

- Shows a history of commits.

### git push

- Pushes changes from the local repository to a remote repository.

```
git push                    ==> push to remote repo with current branch name.
git push <remote> <branch>  ==> push change from local branch to specific branch on remote repo.


// Learn later
--prune                     ==> remove remote branches that don't have local counterpart.
-d | --delete               ==> all listed refs are deleted from the remote repo.
--tags                      ==> all refs under refs/tags are pushed.
-f | --force                ==> force commit even though remote ref is not an ancestor of local ref.(usually git disallows this, --force will skip this check) [DON'T USE AS OF NOW]
```

### git branch

- Lists branches in the local repository.

Extra Flags

```
--list | -l (default)  // ==> List all existing branches (green = current branch)
-a | --all             // ==> All
-r                     // ==> List all remote branches

```

### git checkout

- Switches to a different branch or commit.

```
git checkout <branch>         ==> switch to the specified branch
git checkout -b <new-branch>  ==> creates new branch and switches to it
git checkout -- <file>        ==> discard changes made to a file since last commit and revert it to last committed version
git checkout -- .             ==> discard all changes made to the file in the working directory since last commit and revert them to the last committed version

// Learn Later
--detach
```

### git fetch

- Fetches changes from a remote repository without merging them.

```
git fetch origin branch-name    ==> fetches changes from a specific branch on the remote repo to your local repo
--all                           ==> fetches changes from all remote repo to local repo
--prune                         ==> fetches changes from the remote repo and removes any references to branches that have been removed in remote
--tags                          ==> fetches all tags from the remote repo to local repo
```

### git merge

- Merges changes from one branch into another.

```
git merge <branch>

--abort                             ==> abort current conflict resolution process
--continue                          ==> conclude the merge, whet git merge stops due to conflict.

--commit | --no-commit              ==> merge and commit the result (no-commit => merge and stop before creating a merge commit)
--edit | -e                         ==> invoke a editor before committing successful mechanical merge
--cleanup                           ==> determines how message will be cleaned up before commiting


// Learn later
--ff
--no-ff
--squash                            ==> squash all commit from branch merging into one commit
--ff-only
--stat
```

### git pull

- Fetches and merges(or rebase) changes from a remote repository.

```
git pull origin <branch_name>


--rebase
--no-rebase
--ff-only
--ff
```

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
