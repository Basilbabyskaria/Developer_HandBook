# Commands

## Repo (Repository)
Folders which are tracked by git

## Commands

### Config
`git config --gobal user.name "<name>"`  
`git config --gobal user.email "<email>"`  
`git config --gobal core.editor "code  --wait"` setting default editor to vs code  
Data is stored in .gitconfig file

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
Git Follows atomic commits(Focused on one thing)  
Keep commits centric to one feature, one component or one fix  
Each commit is dependent on the previous commit except for the intitial.

### Log
`git log` Gives log of commits  
`git log --oneline` Gives log of commits in oneline

### Git Ignore
Create a file as `.gitignore` and names of files in it which should be ignored by git  
Sensitive files like API key can be stored here

### Branch

`git branch` list banches of current project  
`git branch <branch_name >` create a new branch  
`git checkout <branch_name >` to change branch's or `git switch <branch_name>`  
`git branch -d <branch_name >` deletes the branch

### Merge
`git merge <branch_name> -m "message"` brings code from a branch and merges to current branch  
