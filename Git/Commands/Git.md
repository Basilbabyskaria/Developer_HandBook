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

`git init` initialize's git on the current repository (one time per project)  
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

### Git Diff

Used to compare a file in different circumstances(between different commits or different branchs)  
`-`,`+` Does not represents rows removed or added both represents the two different files ,`-` represents first and `+` the second  
`git diff --staged` checks difference between files in staged and commited state  
`git diff commit_ID1 commit_ID2` checks difference in files from different commits,ID's are taken from oneline log  
`git diff branch1 branch2` checks difference in files from different branchs

### Stashing

When you are working on a branch and need to do some task on an another branch or even the main branch without commiting the current branch  
`git stash` stash's the current branch  
`git stash pop` Bring's it back  
U can pop stashed branch's to any branch's irrespective of where it is created  
`git stash list` list's stashes  
`git stash apply "stash to pop"` can be used to pop a specific stash

### CheckOut

Other than it's function of switching branchs it can be used to switch between commit's  
`git checkout commit_id`  
`git checkout HEAD~2` look at 2 commits prior  
`git checkout branchname` ,`git reflog`to get back

### Restore

`git restore filename` get the file back to it's just previous commit version and not more

### Rebase
Rewrites history and clean up commits
It rebases current branch with specified branch which means it's literly merging and removing history so never run it while in master branch  
Usually used when you are working on a branch while lots of changes where made on the master branc and you need to bring that changes to your current branch  
`git rebase master` rebase the branch you are curently in with the maaster branch  
conflicts resalution is same as when we merge  
But need to `git add file ` and `git rebase --continue`

### Git Hub
It's an online service which hosts git in to a cloud environment  
It is mainly used for collaburation,open sourceing and safe keeping of projects  
to start using git hub and your device together you need to connect both via ssh  
search web to do it

### Basic Commands
`git remote -v` To check if current project allready have a remote counter part  
`git remote add name url`  used to link current project to a repository which is created in git hub  
Repository should be created withh github web site for doing this  
`name` Is usually put as origin and url is obtained when the repository is created  
`git remote rename oldname newname` To Rename  
`git remote remove name` To remove  
`git push origin branchname` To push data to remote branch aka git hub repository  
`git push -u origin main` Here `-u` is called upstream if we add this when pushing one time after which you can simple do `git push` with out specifying to where  
`git clone url` to clone a github  repository to your device  

### Pull Fetch
`git fetch origin main` Get's info of file in repository but does not merge to local file  
git pull =git fetch + git merge  
`git pull origin main` Fetches the files and add it tp your work  
Both are used when you are actively contributing and u need to update on the changes made onn the repository by others  
