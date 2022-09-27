<h1 align="center">Part 1</h1>

## Undoing Stuff & Time Traveling

### **Checkout**
We can use checkout to create branches, switch to new branches, restore files, and undo history!
We can use *git checkout commit <commit-hash>* to view a previous commit.
```console
git checkout <commit-hash>
# or
git checkout HEAD~<number>
```
> HEAD~1 refers to the commit before HEAD (parent)

> HEAD~2 refers to 2 commits before HEAD (grandparent)

- `Detached HEAD`
	Usually, HEAD points to a specific branch reference
	rather than a particular commit.
	When we checkout a particular commit, HEAD points at that commit rather than at the branch pointer.
	You have a couple options:
	- Stay in detached HEAD to examine the contents of the old commit.  Poke around, view the files, etc.
	- Leave and go back to wherever you were before - reattach the HEAD
	- Create a new branch and switch to it.  You can now make and save changes, since HEAD is no longer detached.

	If you checkout an old commit and decide you want to return to where you were before Simply switch back to whatever branch you were on before.
```console
git switch <branch-name>
# or 
git switch -
```

- `Discarding Changes`
	Suppose you've made some changes to a file but don't want to keep them.  To revert the file back to whatever it looked like when you last committed, you can use:
```console
git checkout HEAD <files>
# or
git checkout -- <files>
```

### **Restore**
git restore is a brand new Git command that helps with undoing operations.

-  `Unmodifying Files with Restore`
	Suppose you've made some changes to a file since your last commit. You've saved the file but then realize you definitely do NOT want those changes anymore! To restore the file use this:
```console
git restore <file-name>
```
> NOTE: The above command is not "undoable" If you have uncommited changes in the file, they will be lost!
	
git restore <file-name> restores using HEAD as the default source, but we can change that using the --source option.

```console
git restore --source <commit-hash-or-HEAD~N> <filse>
```

- `Unstaging Files with Restore`
If you have accidentally added a file to your staging area with git add and you don't wish to include it in the next commit, you can use git restore to remove it from staging.
```console
git restore --staged <file-name>
```	
