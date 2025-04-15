## GIT CHEATSHEET

<img src="push.png" width="700" height="400" />

#### 1. When you want to push a locally residing code to your remote repo:
`git init` create the local repository  
`git add filename` or `git add .` to add all the files in the pwd to the staging area  
`git commit -m "Commit message"` commit changes to your local repository  
`git remote add origin  <REMOTE_URL>` point to your github (or any other remote) repo  
`git push -u origin master` this command pushes your changes to your remote repo  

#### 2. Fetch remote changes and rebase your local commits  
*Note:* Make sure to commit your local changes beforehand.  
**Option 1 - More controlled**  
```git
git fetch origin
git log origin/development-branch  # inspect what's new
git rebase origin/development-branch
```

**Option 2 - Quick and simple**  
`git pull --rebase origin development-branch`

---

* `git remote -v`  get a list of any configured remote URLs.  

* `git log` see all the commits that were made for our project  

* `git status` shows the state of the working directory and the staging area; which changes have been staged, which haven't, and which files aren't being tracked by Git  

* `git branch <new-branch-name>` creates a new branch  
  `git branch` lists the current branches for your project  
  * `-d <branch-name>` deletes the *branch-name*
  * `-vv` shows remote tracking branch per local branch
  
* `git checkout` is a local operation that only operates on data that's already fetched  
  `git checkout <commit-hash>` go back to a previous state of your project code that you committed  
  `git checkout <branch-name>` switches to a different branch  
  `git checkout -b ＜new-branch＞` create the new branch and immediately switch to it  
  
  **Git Checkout a Remote Branch**: first fetch the contents of the branch  
  ```git
  git fetch --all  
  git checkout ＜remotebranch＞
  ```
* `git merge <branch-name>` replace *branch-name* with the branch that you want to integrate into your current branch  
* `git fetch` view the changes made in the remote repository without making any local changes  
* `git pull` add remote changes to local repository  
