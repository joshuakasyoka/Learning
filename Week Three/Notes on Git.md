<h1>Notes on Git from Documentation</h1> 

<h2>Links</h2>

- [x] The Net Nija: https://www.youtube.com/watch?v=HbSjyU2vf6Y

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
* `git branch -a` again allows us to view and switch to selected branch
*  `git checkout master` allows us to see master branch again 
*  `git checkout out <namebranch>` then takes us to branch again
*  `git branch -D <namebranch>` deletes our branch 
*  `git checkout -b <namebranch>` names branch and check its out, doing two function in one: creating branch and moving to it 

<h3>Merging Branches</h3>

* `git merge <namebranch>` allows us to merge to the master branch (which we are merging from)
*  we sometimes come across git conflicts when someone has updated the master while another person has been working on a branch, then we will have to resolve the difference

<h3>Github</h3>

* `git push <https://url> master` allows us to push to a remote repository and it sets up a new 'master' 
* `git add .` > `git commit -m "message"` > `git push <https://url> master` allows us to update our repository
* Instead of using the whole url every time, we have to do `git remote add origin <https://url> master`, then we can just use `git push origin master`
* If we don't already have an existing repository we can use `git clone <https://url>` which makes it now local on our computer
* we don't have to set up an orgin alias with cloned applications, so we just use `git push`

<h3>Collaborating on Github</h3>

* `git pull origin master` fetches all the code from the remote and allows us to work on it remotely... remote > local
* `git checkout -b index-html` creates a new branch `index-html` and allows us to add new features without having an effect on the main branch. 
* `git push origin index-html` will push up a specific branch to the remote and allow for it to be checked before merging 
* we always need to 'pull' the master branch incase there are changes
* we shouldn't merge branch to master locally beacuse that will change the code for everyone. 

<h3>Forking and Contributing</h3>

* Forking allows us to copy a repository from another person's account into our own...
