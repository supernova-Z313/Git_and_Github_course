<h1 align="center">Part 2</h1>

<h3>Viewing Branches</h3>
Use *git branch* to view your existing branches. The default branch in every git repo is master, though you can configure this.

```cosole
git branch
```

- use -v flag to see more good details about each branch

<h3>Creating Branches</h3>
Use git branch <branch-name> to make a new branch based upon the current HEAD.
This just creates the branch.  It does not switch you to that branch (the HEAD stays the same).

```cosloe
git branch <branch-name>
```

<h3>Switching Branches</h3>
Once you have created a new branch, use git switch <branch-name> to switch to it.

```console
git switch <branch-name>
```
Historically, we used git checkout to switch branches.  This still works.
```cosloe
git checkout <branch-name>
```

<h3>Creating & Switching</h3>
Use git switch with the -c flag to create a new branch AND switch to it all in one go.

```cosloe
git switch -c <branch-name>
```
> Note: -c = create

or do it in old way

```cosole
git checkout -b <branch-name>
```
> Note: -b = boy or branch

<h2>Warning</h2>

If you make changes in a file and don't commit them, when you switch to another branch, all this information will be deleted, so we must commit or stash the changed information.
Also, if you create a new file and do not commit it, the file will be transferred to any branch you switch to, until you commit it in one of the branches.

<h3>Deleting</h3>

To delete a branch, just use the following command:

```cosole
git branch -d <branch-name>
```

- To delete a branch, we must not be in that branch.
- If we don't merge a branch, we should use -D flag to delete it.

<h3>Renaming</h3>
To change the name of a branch, we must be present in that branch and run the following command:

```cosole
git branch -m <branch-name>
```

#

> Note:
>  We can add all file and changes to stage and commit them with one line code :
> ```cosole
> git commit -a -m "message"
> ```
> use flag -a to do it in one line.


