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
git log -patch
git log -stat

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
git clean
```    
</details>


