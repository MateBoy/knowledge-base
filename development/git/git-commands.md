Some nice-to-have Git commands.  
For more, see [Git Flight Rules](https://github.com/k88hudson/git-flight-rules).

#### I want to see the current status of my repository
```
$ git status
```

#### I want to commit all modified files and add a commit message
```
$ git commit -a -m "Commit message"
```

#### I want to commit all modified files and add a commit message and description
```
$ git commit -a -m "Commit message" -m "Commit description"
```

#### I want to add all untracked file to my repository
```
$ git add .
```

#### I need to switch branch but don't want to commit my work-in-progress changes
```
$ git stash
```

Then, when you need to re-apply the stash:
```
$ git stash apply
```

And finally, when all looks good and you want to delete your stash:
```
git stash drop
```

#### I want to list all existing remote branches
```
$ git branch -r
```

#### I wrote the wrong thing in a commit message
```
$ git commit --amend --only -m 'New commit message'
```