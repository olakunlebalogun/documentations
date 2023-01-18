# Git Command Documentation

## Installing on Linux  
`apt install git`

## Configuring git Identity  
`git config --global user.name = "Olakunle" `  
`git config --global user.email = olakunle@gmail.com`  
`git config --global core.editor vim`

To list the configurations   
`git config --list`

To get the value of a single config e.g username  
`git config user.name`

To set the value of a single config e.g core.editor  as say vim  
`git config --global core.editor vim`


## Getting Git Documention and Manual  
Use either of these commands
* `git help <verb>`
* `git <verb> --help`
* `man git-<verb>`  
verb here means a git command e.g init, commit etc.



## Git Init
Git initialization, this is to initialize a project to be git   enabled.  

This is to initialize with master as default branch  
`git init`

To initialize with a named branch as default branch  
`git init -b branchName`

## Git Clone

To clone project from a remote repository  
`git clone [url]`  

To clone a project from a remote repository with your own folder-name  
`git clone [url] <folder-name> `  



## Git Status
This is to get the status of the project the that point in time 
  
To get the status  
`git status`

To get the short format of the status  
`git status --short` OR `git status -s`  
**N:B** The short option has some special notations:
* M means *modified*
* A means *Added to staging area*
* ?? means *untracked file*
* M means *modified*

e.g

```
$ git status -s     
 M README  
MM Rakefile
A lib/git.rb
M lib/simplegit.rb
?? LICENSE.txt

New files that aren’t tracked have a ?? next to them, new files that have been added to the staging area have an
A, modified files have an M and so on. There are two columns to the output—the left hand column indicates that the
file is staged and the right hand column indicates that it’s modified. So for example in that output, the README file is
modified in the working directory but not yet staged, while the lib/simplegit.rb file is modified and staged. The
Rakefile was modified, staged and then modified again, so there are changes to it that are both staged and unstaged
```



To get the long status format  
`git status --long`
 
To get the ignored files at the moment
`git status --ignored`


## Git Ignorefile

Craete a git ignore file using  
`cat .gitignore` OR `vim .gitignore`

Patterns in gitignore file
*  \# - This denotes comments in the ignore file  
*  / - This denotes the start of a directory
*  REGEX patterns
*  ! - This negates the declared REGEX pattern


```
# a comment - this is ignored
*.a
# no .a files
!lib.a
# but do track lib.a, even though you're ignoring .a files above
/TODO
# only ignore the root TODO file, not subdir/TODO
build/
# ignore all files in the build/ directory
doc/*.txt # ignore doc/notes.txt, but not doc/server/arch.txt
```

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

To unstage a file  
`git `

## Unstaging files
To remove a file from the staging area e.g index.html  
`git rm -cached index.html`

To remove set of files with directory from the staging area  
`git rm -r -cached .`

## Git Diff  

To compare what is in your current working directory that are **not** staged and your last commit  
`git diff`  

To show changes that are staged for the next commmit  
`git diff --staged`  

To show changed that have been staged
`git diff --cached`

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

> Commit hash is the string of hexadecimals using SHA-1 attached to each commit


## Git Log
To view all the commits  
`git log`

To see the last **n** commit   
`git log -n`

To see the difference in each commits  
`git log -p`

To see the abbreviated stats for each commits  
`git log --stat`  

To print each commit in a single line  
`git log --pretty=oneline`

To format your commits use the *format* options
`git log --pretty=format: "%h - %an, %ar : %s"`  

Other format options

|**Options**| **Description** |
|-------|--------------------------------|
| %H  | Commit Hash |
| %h  | Abbreviated commit hash |
| %T  | Tree hash  |
| %t  | Abbreviated tree hash  |
| %P  | Parent hash  |
| %p  | Abbreviated parent hash |
| %an | Author name |
| %ae | Author email |
| %ad | Author date |
| %ar | Author date, relative |
| %cn | Commiter name |
| %ce | Commiter eamil |
| %cd | Commiter date e.g May 20, 2022 |
| %cr | Commiter date, relative e.g 2 days ago |
| %s  | Subject |


To get a graphical representation  
`git log --graph`  


Other options for the **log** command
| **Option** | Description |
|------------|--------------------------------------------------|
| -p  | Show the patch introduced with each commit |
| --stat | Show statictics for files modified in each commit |
| --shortstat  | Display only the changed/insertions/deletions line from the --stat command |
| --name-only  | Show the list of files modified after the commit information |
| --name-status | Show the list of files affected with added/modified/deleted infromation as well |
| --abbrev-commit  | Show only the first few charecters of the SHA-1 checksum instaed of all 40 |
|--graph  | Display an ASCII graph of the branch and merge history beside the log output |
| --relative-date | Display the date in a relative format e.g 2 days ago, instead of using the full date format |
| --pretty | Show commits in an alternate format. Otions include oneline, short, full, fuller and format(where you specify your own format)

To restore the changes to the last commit  for a file  
`git restore filename`

To restore the changes to the last commit for for the whole project  
`git restore .`

To show thw difference between the present changes and the last commit  
`git diff` 

##  File Removal and Deletion

To remove a file from the working directory, aslo so that git won't tracked it anymore  
`git rm filename`  

If the file had been modified added to the staging area already use  
`git rm -f filename`

To want git to **untrack** a file, but it should stilll be present in the working directory  
`git rm --cached filename`

## Moving Files in Git

To move file in git  
`git mv filename file-destination-path`  

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
 git switch -c <new-branch-name>
  git switch -


Updated for Git 2.23: For older versions, see the section at the end.

With One Remote
In both cases, start by fetching from the remote repository to make sure you have all the latest changes downloaded.

$ git fetch
This will fetch all of the remote branches for you. You can see the branches available for checkout with:

$ git branch -v -a

...
remotes/origin/test
The branches that start with remotes/* can be thought of as read only copies of the remote branches. To work on a branch you need to create a local branch from it. This is done with the Git command switch (since Git 2.23) by giving it the name of the remote branch (minus the remote name):

$ git switch test
In this case Git is guessing (can be disabled with --no-guess) that you are trying to checkout and track the remote branch with the same name.

With Multiple Remotes
In the case where multiple remote repositories exist, the remote repository needs to be explicitly named.

As before, start by fetching the latest remote changes:

$ git fetch origin
This will fetch all of the remote branches for you. You can see the branches available for checkout with:

$ git branch -v -a
With the remote branches in hand, you now need to check out the branch you are interested in with -c to create a new local branch:

$ git switch -c test origin/test
For more information about using git switch:

$ man git-switch
I also created the image below for you to share the differences, look at how to fetch works, and also how it's different to pull:

enter image description here

Prior to Git 2.23
git switch was added in Git 2.23, prior to this git checkout was used to switch branches.

To checkout out with only a single remote repository:

git checkout test
if there there are multiple remote repositories configured it becomes a bit longer

git checkout -b test <name of remote>/test















## GIT SUBMODULE
