
Create new branch
``git branch <branchname>`` 

Switch to branch
``git checkout <branchname>``

Create and directly switch to a new branch
``git checkout -b <branchname>`` 

Merge a branch
```
git checkout main
git merge <branchname>
git branch -d <branchname>
```

Rename branches (master to main)
```
git branch -m master main
git push -u origin main
```
