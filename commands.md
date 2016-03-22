#Git Commands

##Create repo in pwd
git init

##Print status
git status

##Add file/s to staging area
git add octocat.txt
git add '*.txt'

**Note: the quotes are necessary to prevent the shell from capturing the wildcard and only searching within the current directory**

##Add all to the staging area
git add -A .

##Delete files and stage their removal
git rm '*.txt'
git rm -r *foldername*

#Auto remove deleted files with commit (if deleted without using rm)
git commit -am "delete stuff"

##Reset staging area - remove a file or files from the staging area
git reset *filename*

##Commit to repo
git commit -m "Add cute octocat story"

##Print log of commits
git log
git log --summary *(shows more information about each commit)*


##Add a remote repo
git remote add origin https://github.com/try-git/try_git.git

**Note: origin is the name of the remote repo (origin is a typical name for the main one)**

##Pushing to remote repo
git push -u origin master

**Note: -u tells Git to remember the parameters so that next time you can simply run git push**

##Pull changes from remote repo
git pull origin master

##Git stash
sometimes when you go to pull you may have changes you don't want to commit just yet. One option you have, other than commiting, is to stash the changes.

Us the command 'git stash' to stash your changes and 'git stash apply' to re-apply your changes after your pull.

##Compare pwd to local repo
git diff HEAD

**Note: HEAD is a pointer to the most recent commit. Othewise you have to use the SHA reference**

##Compare staged files to local repo
git diff --staged

##Undo (get rid of all changes since last commit for octocat.txt)
git checkout -- octocat.txt

##Creating a branch
git branch mybranch

##Print branches
git branch

##Switch to a branch
git checkout mybranch

##Create and checkout branch at same time
git checkout -b mybranch

##Merging branches into master
###Switch back to master
git checkout master

###Merge the branch into master
git merge mybranch

##Delete a branch
git branch -d mybranch
git branch -D mybranch *or* git branch -d -f mybranch  *(for branches that haven't been merged)*

