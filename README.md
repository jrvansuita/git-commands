# git-commands
a bunch of git commands from basics to advanced ones.


## Setup
<details open><summary><b> Init git repository </b></summary>
  
> Inside the desired folder
  
```
git init
```    
</details>

<details open><summary><b> Delete .git/ folder </b></summary>
  
```
rm -fr .git/
```    
</details>


## Configs
<details open><summary><b> Setting user name and email </b></summary>

> Can be user with user.name or user.email

```
git config --global user.email "me@email.com"
```    
</details>

<details open><summary><b> Change default branch name to "main" </b></summary>

```
git config --global init.defaultBranch main
```    
</details>


### File Staging
<details open><summary><b> Get git status </b></summary>

```
git status
```    
</details>

<details open><summary><b> Stage files </b></summary>

> Add all files or one by one
  
```
git add .
git add hello.txt
```    
</details>

<details open><summary><b> Unstage files </b></summary>
  
> Unstage all files or reset all
  
```
git restore --staged .
git reset --hard
```    
</details>


<details open><summary><b> Unstage files without Head </b></summary>

> Unstage all files or one by one
  
```
git rm --cached -r .
git rm --cached -r hello.txt
```    
</details>


## Commiting

<details open><summary><b> Commit </b></summary>
  
```
git commit -m "few changes"
```    
</details>

<details open><summary><b> Check diffs </b></summary>
  
> See files diffs when not staged or after staging the files
  
```
git diff 
git diff --cached
```    
</details>

<details open><summary><b> Amend </b></summary>
  
> Change commit message
  
```
git commit --amend -m "updated commit message"
```    
</details>

## Logging

<details open><summary><b> Log </b></summary>
  
> Some usefull log commands. The list is starting from most recent commit to the oldest. HEAD means most recent one.
  
```
git log
git log --oneline
git log -3 
git log --patch
git log --stat

```    
</details>

## Checkout

<details open><summary><b> Checkout </b></summary>
  
> Checking out to a specific commit and returning to the head
  
```
git checkout 3197c04
git checkout main
```    
</details>

<details open><summary><b> Clean Untracked </b></summary>
  
> Remove all untracked files
  
```
git clean -f
```    
</details>


## Remote

<details open><summary><b> Adding Remote </b></summary>
  
```
git remote add origin <url>
```    
</details>

<details open><summary><b> Check Remote </b></summary>
  
```
git remote -v
```    
</details>
  
## Branch

<details open><summary><b> Listing </b></summary>
  
```
git branch
```    
</details>

<details open><summary><b> Create and Checking out a branch </b></summary>
  
```
git branch <new-branch-name>
git checkout <new-branch-name>
  
//Both commands in one line
git checkout -b <new-branch-name>
  
//Both commands in one line using switch command
git switch -c <new-branch-name>
  
//And undo all before chekcing out to a new branch
git checkout -f -b <new-branch-name>
```    
</details>
  
  
<details open><summary><b> Delete </b></summary>
  
```
git branch -D <new-branch-name>
```    
</details>  
  


