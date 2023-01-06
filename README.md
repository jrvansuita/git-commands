# git-commands
a bunch of git commands from basics to advanced ones.


## Setup

```properties
# Init git repository  
git init

# Delete .git/ folder 
rm -fr .git/
```    

## Config

```properties
# Setting user email
git config --global user.email "me@email.com"
  
# Setting user name
git config --global user.name "me"  

# Change default branch name to "main"
git config --global init.defaultBranch main
```    

## SSH
```properties
# Generate key
ssh-keygen

# Adding the generated key
 ssh-add ~/.ssh/id_rsa
```


## Status

> Check the current git status 

```properties
# Gives a detail status from the current work
git status
```    

## Stage

> When the files are staged means they begin been tracked by git and they are ready to be commited.

```properties
# Stage all files 
git add .

# Stage one by one
git add hello.txt
  
# Unstage all files
git restore --staged .

# Unstage and clean
git reset --hard

# Unstage files without a Head commit (When creating the repository)
git rm --cached -r .
git rm --cached -r hello.txt
```    

## Commiting

> Commiting means save your work.

```properties
# Commit with a message
git commit -m "few changes"

# See files diffs when not staged
git diff 

# See files diffs when staged
git diff --cached
  
# Change the last commit message (Not possible to change previous commits)
git commit --amend -m "updated commit message"
```    

## Logging

> Some usefull log commands. The list is starting from most recent commit to the oldest. HEAD means most recent one.
  
```properties
# Shows all the list
git log

# Show only one line
git log --oneline

# Shows the last 3
git log -3 

# Different view
git log --patch

# Simple resume from each
git log --stat
```  

## Checkout

> Checkout command is used to change your current work to a specific commit, tag or even another branch.

```properties
# Checkout to a commit
git checkout 3197c04

# Checkout to a branch
git checkout develop

# Clean untracked files before checking out
git clean -f
```    
 
## Remote

> Adding a remote url is need to share your repository with the team.
  
```properties
# Adding a remote url to the local repository
git remote add origin <url>

# Check remote url attached
git remote -v
```    
  
## Branch
  
> Branch is used to make a copy from the current main branch to start implementing features without messing up with the stable main branch. 
  
```properties
# Listing  
git branch

# Creating and checking out a new branch
git checkout -b <new-branch-name>
  
# Now using switch command
git switch -c <new-branch-name>
  
# Discart all changes before creating and checking out to a new branch
git checkout -f -b <new-branch-name>

# Delete a branch on local
git branch -D <branch-name>

# Delete a branch on remote
git push --delete origin <branch-name>
 
# Renaming the current branch on local
git branch -m <branch-name2>
  
# Renaming a specific branch  on local
git branch -m dev <any-branch-name>
  
# For renaming on remote, you need first delete the branch from remote, 
# rename local with the above command and push again to the remote.  
  
# Push new branch to remote  
git push --set-upstream origin <new-branch-name>
```    

## Merge
   
> When the work is done on a feature branch, you shall merge the work to the develop branch, right? 
  
```properties
# Merge on current branch the work from ...
git merge <feature-branch>

# Aborting when conflicts
git merge --abort
```      
  
## Tags

> It make a mark point on any commit. You can easily checkout a tag (commit) and compare tags with the diff command. It generally stands for marking release versions.
  
```properties
# Listing  
git tag -n
  
# Tagging current commit (HEAD)
git tag v1
  
# Tagging a specific commit
git tag v1 922b10b
  
# Tagging with an annotated tag
git tag -a -m "tag for v1 version" v1  
  
# Pushing v1 to remote
git push origin v1
  
# Pushing all tags to remote
git push origin --tags
  
# Deleting a local tag
git tag -D v2
  
# Deleting a remote tag
push --delete origin v2
```    
  
## Stash

> If you have an unready work and need to start working on another feature, you can stash changed from a specific branch and work on another branch without messing up with the current work.
  
```properties
# Stashing
git stash
  
# Listing
git stash list
  
# Applying  
git stash apply
  
# Applying a specific one 
git stash apply stash@{2}
  
# Applying and Deleting
git stash apply pop
  
# Deleting
git stash drop stash@{2}
```    

## Revert

> Use revert command to revert a commit or reset command to delete and not keep track of commits history.

```properties
## Revert last commit and keep history
git revert HEAD --no-edit

# Delete 1 commit from head, destroy history.
git reset --hard HEAD~1

# Forcing a push for updating remote with new history
# Whenever there are history change on commits, it's necessery to use --force
git push --force

# Check if there are not changes lost on the process 
git push --force-with-lease
```

## Rebase

> Rebase is used to change the initial content after you have commits on your branch. Mostly used to merge main commits on you feature branch before merging your own commits on main branch. So that, git will not create the merge commit.

```properties
# On your current feature branch
git rebase main

# Pull the rebase
git pull --rebase
```
  


