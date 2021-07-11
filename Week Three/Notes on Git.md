<h1>Notes on Git from Documentation</h1> 

<h2>Notes</h2>

<h3>making commits and tracking them</h3>
* `git init` initialises a repository locally and this is represented by '.git' in project folder
* `git status` allows us to see our current repo status, what has and has not been staged
* `git add .` adds all files to the staging area 
* `git add <file name>` allows us to commit one file at a time
* `git rm --cached <file>` allows us to remove items from the staging area 
* `git commit -m "message"` allows us to commit a instance to the repo... all these files are made to the master branch 
* `git log` allows us to see all the different commits we have made... shows the unique id 
* `git log --oneline` shortens our commits into more digestable chunks 

<h3>reverting changes</h3>
* `git checkout <af5b84c>` allows us to revert back to earlier commit and see the state of the code 
* `git checkout master` then allows us to move back to the master branch and code before we reverted back.
* `git revert <af5b84c>` and then use `:wq` 
* `git reset <af5b83z> --hard` will delete commits
* up arrow allows us to go to previous command in command line

<h3>branches</h3>
* master branch is usually the code we do not want to be experimental on 
* git branch lets us move away from the main branch and edit, without effecting the main branch 
* `git branch <namebranch>` allows us to create new branch
* `git branch -a` allows us to select which branch we work on
* usually we will be on `*master` e.g. master branch 
* `git checkout <namebranch>` takes us onto selected branch 
* `git branch -a` again allows us to switch to this selected branch
*  `git checkout master` allows us to see master branch again 
*  `git checkout out <namebranch>` then takes us to branch again
*  `git branch -D <namebranch>` deletes our branch 
*  `git checkout -b <namebranch>` names branch and check its out, doing two function in one: creating branch and moving to it 

<h3>Merging Branches</h3>
*
