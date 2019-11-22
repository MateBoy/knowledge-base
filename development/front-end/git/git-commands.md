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

#### I want to list all existing remote branches
```
$ git branch -r
```

#### I wrote the wrong thing in a commit message
```
$ git commit --amend --only -m 'New commit message'
```