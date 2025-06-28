## reflog (Reference Log)

Git keeps a history of where `HEAD` has pointed in a file called `.git/logs/HEAD`, and it’s human-readable. It records every move of a reference like `HEAD`.
Git also keeps the history of the tip of each branch locally.

> Note: Git only keeps reflogs of your **local activity** — they’re not shared with collaborators.

> Note: Reflogs expire. Git automatically cleans these logs after **90 days**.

```bash
# View the reflog of a pointer (like HEAD)
git reflog show HEAD
```

The commits you delete, reset, or rebase won’t appear in `git log` anymore — but `git reflog` keeps track of every move of references like `HEAD`, so you can recover those commits if needed.

### Accessing Specific Reflog Entries

You can reference a specific point in the reflog history using the syntax `name@{qualifier}`.

For example:

* `HEAD~2` means the grandparent (2 commits before) of the current `HEAD` — **by position in the commit graph**.
* `HEAD@{2}` means where `HEAD` pointed **2 moves ago**, which may still be the same commit if no new commit was created.

Each reflog entry has a timestamp, and you can use it like this:

```bash
main@{yesterday}
main@{2.days.ago}
master@{1.week.ago}
```

---

### Undoing a `git reset --hard` with Reflog

When you use `git reset --hard` to delete a commit and its changes, the commit isn’t actually erased from your repository.
It still exists in the `.git/objects` directory — but without a parent, it’s orphaned and inaccessible via normal commands.

To recover it:

1. Use `git reflog` to find the commit hash or the reflog reference.
2. Use `git reset --hard` to move `HEAD` back to that point:

```bash
git reset --hard master@{1}
```

### Recovering After a Rebase

When you undo a `git rebase`, remember that rebased commits still have their parent commits attached.
If you recover a commit from before a rebase, it may bring its parent commits too — depending on how you reset or cherry-pick them.