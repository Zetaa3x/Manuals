GIT manual


Some basic commands
git stage
git add 
git commit
git push
git config

=================
Git configuration
=================
git config --list
	to show config list
e.g after using --list for your element, can specify the search
this command shows your current git user email which is used for identity purposes
git config user.email

e.g pt 2 
git config --list can also show

+ git remote

===== COMMON PROBLEMS ====
PROBLEM:
error: remote origin already exists.
OR
remote: Repository not found.
fatal: repository 'XXX' not found
^ XXX is a placeholder for your github HTTPS or SSH url 

SOLUTION: git remote set-url a b
a = origin or upstream
b = new remote URL 

PROBLEM:
error: src refspec master does not match any
error: failed to push some refs to 'XXX'
OR
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use    

    git push --set-upstream origin main

SOLUTION: git push --set-upstream origin main
(NOTE-> Add in explanation for branches)


======
GITHUB
======

[https://github.com/cli/cli#installation]
installing github cli - on windows using choco
+ Requirements
	+ install choco
choco install gh




