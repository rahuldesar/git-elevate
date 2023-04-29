# GIT BASICS

---

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

### git fetch

- Fetches changes from a remote repository without merging them.

### git merge

- Merges changes from one branch into another.

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

- Lists the remote repositories.

### git reset

- Resets changes in the staging area or working directory.

### git stash

- Stashes changes in a temporary area.
