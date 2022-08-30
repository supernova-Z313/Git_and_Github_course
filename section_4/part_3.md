<h1 align="center">Part 3</h1>

<h3>Amending Commits</h3>

Suppose you just made a commit and then realized you forgot to include a file! Or, maybe you made a typo in the commit message that you want to correct.

Rather than making a brand new separate commit, you can "redo" the previous commit using the --amend option.

> --amend option is just for change last commit.

for use --amend we should first add file to stage and then use this command:

```console
git add forgotten_file
git commit --amend
```
	
