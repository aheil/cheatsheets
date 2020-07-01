
##Create new branch
``git branch <branchname>`` 

##Switch to branch
``git checkout <branchname>``

##Create and directly switch to a new branch
``git checkout -b <branchname>`` 

##Merge a branch
```
git checkout main
git merge <branchname>
git branch -d <branchname>
```

##Rename branches (master to main)
```
git branch -m master main
git push -u origin main
git push origin --delete master
```

If you end up with 
```
 ! [remote rejected] master (refusing to delete the current branch: refs/heads/master)
```
got to GitHub Settings/Branches and swith the default branch to main
Try the previous command again.

##Create Repos out of local folder

1. Create remote repo (e.g. GitHub) and copy remote repo URL

```
git init
git add <file>
git commit -m "initial checkin"
git remote add origin remote <remote URL>
git remote -v
git push origin master
```

There might be an error 

```error: failed to push some refs to <remote URL>```

This shoud not happen if you have added and commited a file as above. 
Git creates its master branch only after the commit to the local repository. 
If you just initialize the repository, the master is not created yet.

```
git add .gitignore 
git commit -m "gitignore added"
```

No again try 

```
git push origin master
```










