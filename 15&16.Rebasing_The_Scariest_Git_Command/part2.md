## 📌 Rebase (Interactive)

### What is it?

A **cleanup tool** for when you want to:

* **Rewrite**, **delete**, **rename**, or **reorder commits** before sharing them.

You run rebase in the **current branch** and adjust its commit history.

### How It Works

When using **interactive rebase**, Git opens your default text editor with a list of recent commits and instructions in the comments.

You can choose actions for each commit using these options:

| Command  | Description                                                                      |
| :------- | :------------------------------------------------------------------------------- |
| `pick`   | Use the commit as is.                                                            |
| `reword` | Keep the commit but change its message.                                          |
| `edit`   | Pause to edit the commit’s content.                                              |
| `squash` | Combine this commit with the previous one and let you edit the combined message. |
| `fixup`  | Combine this commit with the previous one but discard this commit’s message.     |
| `drop`   | Remove the commit entirely.                                                      |

*(You can see these options listed in the editor when you start the rebase.)*


### Example:

```bash
# -i means interactive
# HEAD~4 means rebase the last 4 commits
git rebase -i HEAD~4
```

This will open an editor showing the last 4 commits in the current branch.
You can then adjust them as needed.

---

**💡 Pro tip:**
Use interactive rebase before pushing a branch to clean up your commit history, squash WIP (work-in-progress) commits, and make your Git logs tidy and meaningful.

**🚨 Important:**
Only use this on **local or private branches** — avoid rebasing shared or public branches.

