# GIT BASICS

---

THIS DOESNOT COVER ALL GIT COMMANDS AND FLAGS.

To list all available commands or additional help check

```
 man git || git --help || git help -a || git help -g || git help <concept|command>
```

To checkout details about each command use:

```
man git-<command> || git help <command>
// man git-commit || git help commit
```

This is tailored to my own progress, that you might find this helpful.

---

## git init

- Initializes a new Git repository.

```
--template=<template_directory>
```

## git clone

- Clones an existing Git repository.

```
-l | --local            ==> repo is on local machine
-b | --branch <name>    ==> points cloned repo's head to <name> branch

// Learn Later
--depth <depth>
--shallow-since=<date>
--no-tags
```

## git add

- Adds changes to the staging area.

```
.                     ==> Add everyfile to staging
-A | --all            ==> Add all changes to staging area
-p | --patch          ==> selectively add changes within a file to staging area

// Learn Later
-u | --update         ==> updates the index with changes of tracked files.
```

## git commit

- Commits changes to the local repository.

## git push

- Pushes changes from the local repository to a remote repository.

## git pull

- Fetches and merges changes from a remote repository.

## git status

- Shows the status of the working directory and staging area.

## git log

- Shows a history of commits.

## git branch

- Lists branches in the local repository.

Extra Flags

```
--list | -l (default)  // ==> List all existing branches (green = current branch)
-a | --all             // ==> All
-r                     // ==> List all remote branches

```

## git checkout

- Switches to a different branch or commit.

## git merge

- Merges changes from one branch into another.

## git remote

- Lists the remote repositories.

## git fetch

- Fetches changes from a remote repository without merging them.

## git reset

- Resets changes in the staging area or working directory.

## git stash

- Stashes changes in a temporary area.
