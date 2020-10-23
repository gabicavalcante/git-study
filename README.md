# git-study

#### undo git add before commit
```
git restore --staged <file>
```

#### undo last commit before push
```
git reset HEAD~1
```
Use the argument `--hard` to remove all changes (be carefull).

If you only want to update something that you forgot or want to change the commit message, you could use:
```
git commit --amend
```

#### undo a commit after push
Creates a commit that reverts the commit.
```
git revert <commit-ish>
```

#### undo git pull
`git pull` is the same as `git fetch && git merge` so, you can use:
```
git reset --hard
```
Don't forget you can give arguments to specify things such as a particular point in time.

!!! Be careful when using `git reset --hard` because it removes all uncommitted changes.

#### pull without `merge`
```
git pull --rebase
```

#### get changes from <branch> to current branch without `merge`
```
git rebase <branch>
```