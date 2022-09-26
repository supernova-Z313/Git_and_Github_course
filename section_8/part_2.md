<h1 align="center"> Part 2 </h1>

-  **Stash Apply**
You can use git stash apply to apply whatever is stashed away, without removing it from the stash. This can be useful if you want to apply stashed changes to multiple branches.
```console
git stash apply
```

- **Stashing Multiple Times**
You can add multiple stashes onto the stack of stashes.  They will all be stashed in the order you added them.

- **Viewing Stashes**
run git stash list to view all stashes
```console
git stash list
```

- **Applying Specific Stashes**
git assumes you want to apply the most recent stash when you run git stash apply, but you can also specify a particular stash like git stash apply stash@{N}
```console
git stash apply stash@{<step-number>}
```
- **Dropping Stashes**
To delete a particular stash, you can use git stash drop <stash-id>
```console
git stash drop stash@{<step-number>}
```

- **Clearing The Stash**
To clear out all stashes, run git stash clear.
```console
git stash clear
```
