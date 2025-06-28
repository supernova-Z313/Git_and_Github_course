# Github

### Remote

When you clone a repository from GitHub or add a remote, Git creates a remote reference and usually names it `origin` (you can rename it if you want).

Each remote has two URLs:

* **fetch**: for pulling changes from GitHub
* **push**: for sending changes to GitHub

You can check the list of remotes and their URLs with:

```bash
git remote -v
```

To rename a remote:

```bash
git remote rename <old> <new>
```

### Push

To push your local changes to a remote repository:

```bash
git push <remote> <branch>
# For example
git push origin master
```


### master vs main

In 2020, GitHub changed the default branch name from `master` to `main`.

* If you create a new repository on GitHub **and add a file during creation** like readme.md or gitignore, it will make an initial commit. Since commits must belong to a branch, GitHub names this default branch `main`.
* In local Git installations, the default branch name is still `master`.

It’s not a big deal — you can either:

* Change the default branch in your GitHub repository settings, or
* Rename your local `master` branch to `main` with:

```bash
git branch -M main
```

This command renames the current default branch to `main` and updates the default branch setting, no matter which branch you’re currently on.
