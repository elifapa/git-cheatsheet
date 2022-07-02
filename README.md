## GIT CHEATSHEET
![Git CheatSheet](push.png)

#### 1. When you want to push an existing locally residing code to your remote repo:
`git init` create the local repository  
`git add filename` or `git add .` to add all the files in the pwd to the staging area  
`git commit -m "Commit message"` commit changes to your local repository 
`git remote add origin  <REMOTE_URL>` point to your github (or any other remote) repo  
`git push -u origin master` this command pushes your changes to your remote repo  

* `git log` see all the commits that were made for our project  
