Sometimes, I do commit changes I did, but only want to do so temporarily. This is the case, for example, when wanting to change a branch, but having changes in the current branch, where `git stash` is not an option (e.g. because there are untracked files present). 

To undo this commit, simply use

```git
git reset HEAD^
```
