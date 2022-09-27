<h1 align="center"> Part 1 </h1>

When we are in a branch and we make some changes and then we need to change the branch, but we don't want to commit the changes made, so 2 situations happen:
1. changes come with us to the destination branch.
2. Git won't let us switch if it detects potential conflicts.

## Stashing

Git provides an easy way of stashing these uncommitted changes so that we can return to them later, without having to make unnecessary commits.

- **Git Stash**
git stash is super useful command that helps you save changes that you are not yet ready to commit.  You can stash changes and then come back to them later.
Running git stash will take all uncommitted changes (staged and unstaged) and stash them, reverting the changes in your working copy.
```console
git stash
# or
git stash save
```

after that we have stashed changes, we can switch branches, create new commits, etc.
When we done, we can re-apply the changes we stashed away at any point.

- **Stashing**
Use git stash pop to remove the most recently stashed changes in your stash and re-apply them to your working copy.
```console
git stash pop
```
