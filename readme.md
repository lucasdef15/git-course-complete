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
master is the name of the branch