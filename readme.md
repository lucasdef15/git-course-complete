## Creating an Online Backup

local repository refers to thing on my computer.

remote repository refers to things that are online


since there's the local and remote repositories first we need to create the repository on github manually then we need to go to our local repository and give the command:

_git remote add origin https://github.com/lucasdef15/git-course-complete.git_

the name __origin__ is a convention and the url we provide the url that is generated for the repository

next command we can use is:

_git remote_

this command gives us a list of remote repositories that are currently linked, if we want more details we can use:

_git remote -v_

if we want to remove a link to a remote repository:

_git remote remove origin_

### Uploading to GitHub

- Upload to GitHub = push
- Download from GitHub = pull

the next step here is to give our credentials username:

_git config --global credential.username "lucasdef15"_

next:

_git push origin master_

here origin is the name we linked earlier.
master is the name of the branch, can be also be called main.

with __git push__ we push 1 branch of commits at a time

## GitHub Features

video time: 15:34

## Sync Changes From Computer to GitHub

video time: 17:19

we use git push in both cases: to initially push our code up to GitHub, and then later on to push new commits up to GitHub as well.

short cut for git push:

_git push origin master --set-upstream_

next time we just need to use: _git push_

<!-- note: -->

git push only pushes commits 
if my changes are not in a commit, then git push won't be pushing anything.

### overwrite the previus commit

_git commit --amend -m "msg here"_

in case we mess up the commit history and we need to overwrite gitHub

_git push origin master -f_

-f = force push


## Sync Changes From GitHub To Computer

video time: 25:12

if we clone our projec to a different directory it'll simulates as we are working on two different computer.

lest call pc1 as the local original repository and pc2 as any other computer.

in pc2 we can clone the project by running: 

_git clone https://github.com/lucasdef15/git-course-complete.git_

then the files are downloaded and we can make changes to it. Given that any change we make can then be added to the staging area and then committed as normal.

after that we can run:

_git push origin master_

if we run: _git log --all --graph_

we can now see on pc2 that everything is pushhed to origin master, but if we run _git log --all --graph_ on pc1 we now see that it is not up tp date. So we run:

_git fetch_

with that if we run again: _git log --all --graph_, we can see that origin/master is ahead of our local copy so we need to run:

_git pull origin master_

and everyhting is up to date now.