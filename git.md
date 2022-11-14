# Git Command Documentation

## Git Init
Git initialization, this is to initialize a project to be git   enabled.  

This is to initialize with master as default branch  
`git init`

To initialize with a named branch as default branch  
`git init -b branchName`

## Git Status
This is to get the status of the project the that point in time 
  
To get the status  
`git status`

To get the short format of the status  
`git status --short`

To get the long status format  
`git status --long`
 
To get the ignored files at the moment
`git status --ignored`



## Git Add
Git add help to add the new changes to the staging area  

To add a single file e.g index.js  
`git add index.js`

To add set of files e.g index.js, app.jsx, circle.yml and style.css  
`git add index.js app.jsx circle.yml style.css`

To add from the current sub-directory alone  
`git add -A`

To add **all** the files worked on in the parent directory  
`git add .`

## Unstaging files
To remove a file from the staging area e.g index.html  
`git rm -cached index.html`

To remove set of files with directory from the staging area  
`git rm -r -cached .`


## Git Commit
This is mark a landmark in a git history  
  
To commit a change after adding to the staging area  
`git commit -m "commit message"`\

> *The commit message is the summary of what has been done.*  

To add and commit in one command   
`git commit -am "commit message"`

To ammend the commit message of a last commit  
`git commit --amend -m "new commit message"`

To show the commit full information  
`git show <commit hash>`

> Commit hash is the string of alphanumerics attached to each commit

To view all the commits  
`git log`

To restore the changes to the last commit  for a file  
`git restore filename`

To restore the changes to the last commit for for the whole project  
`git restore .`

To show thw difference between the present changes and the last commit  
`git diff` 


## Git Branch
This explains branching git

To get the list of branch created by author  
`git branch`

To get the list of **remote** branch(es)  
`git branch -r`

To get all branches  
`git branch -a`

To create a branch named 'monitor'  
`git branch monitor`

To checkout or switch to branch monitor   
`git checkout monitor`

To create and switch to branch supervisor  
`git checkout -b supervisor`

To checkout to the prevoius branch  
`git checkout -`

To delete a branch named monitor  
`git branch -d monitor`

To rename a branch  
`git branch -m <newName>`


<!-- git reset --hard HEAD~1 -->