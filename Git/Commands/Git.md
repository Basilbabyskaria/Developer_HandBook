# Git

## What is Git
It's a free and open source version Control System,Git is a software and GitHub is a Service they are not the same thing.Git keeps track of the changes made to a files so that we can revert to a previous version if something goes wrong.

## Repo (Repository)
Folders which are tracked by git

## Commands

### Status
`git Status` gives current status of git in current repository

### Initialization
`git init` initialize's git on the current repository  (one time per project)  
creates a `.git` folder which is used to track the version

### Tracking
Even Though Git is initialized on the repository Git has not yet began trancking it,  
`git add <file name>` to add the files to the staging area where files are kept beforing commiting.  
`git rm --cached <file name>` to unstage the file

### Commits
`git commit -m <message>` push's the file to repo where they are tracked for changes,Providing a message is compelsory while commiting