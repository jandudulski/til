# Named stash

Stashes could have names!

```
$ git stash
Saved working directory and index state WIP on master: 9cc4953 Initial commit
HEAD is now at 9cc4953 Initial commit
$ git stash list
stash@{0}: WIP on master: 9cc4953 Initial commit
```

vs

```
$ git stash save "WIP on named stash"
Saved working directory and index state On master: WIP on named stash
HEAD is now at 9cc4953 Initial commit
$ git stash list
stash@{0}: On master: WIP on named stash
```
