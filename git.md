
## Create new branch
``git branch <branchname>`` 

## Switch to branch
``git checkout <branchname>``

## Create and directly switch to a new branch
``git checkout -b <branchname>`` 

## Merge a branch
```
git checkout main
git merge <branchname>
git branch -d <branchname>
```

## Rename branches (master to main)
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

## Create repo out of local folder

Create remote repo (e.g. GitHub) and copy remote repo URL

```
git init
git add <file>
git commit -m "initial checkin"
git remote add origin <remote URL>
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

## When you get `fatal: refusing to merge unrelated histories`

```
git pull origin master --allow-unrelated-histories
```

### Debug when something fails 

Run 

```
GIT_TRACE=1 git commit -m -S  "foobar"    
`` 

will get a detailed output of the commands rund by git, you then can run each of them independently. E.g.#

```bash
00:12:33.129974 git.c:418               trace: built-in: git commit -m 'foobar'
00:12:33.156978 run-command.c:643       trace: run_command: gpg --status-fd=2 -bsau 34534EF345eEF
```
you might want to run 

```bash
gpg --status-fd=2 -bsau 34534EF345eEF
```
to find an error.

# Replaing a tag 

```
git tag -d v1.1.0-beta
git push --delete origin refs/tags/v1.1.0-beta
```
Now do your commits 

```
git tag v1.1.0-beta
git push origin v1.1.0-beta
```





