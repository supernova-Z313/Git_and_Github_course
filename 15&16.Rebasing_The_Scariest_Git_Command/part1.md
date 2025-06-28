## 📌 Rebasing

### What is it?

* An **alternative to merging**.
* A **history cleanup tool**.

With `git rebase`, we **rewrite the project history** by moving a series of commits to a new base commit.
This effectively makes a cleaner, linear history without unnecessary merge commits.

**Important:**
Since rebasing rewrites history, it changes commit hashes.

### Example:

```bash
git switch feature
git rebase main
```

This moves the `feature` branch commits on top of the latest `main` branch commits.

**Before:**

```
A---B---C  (main)
     \
      D---E  (feature)
```

**After:**

```
A---B---C (main) ---D'---E'  (feature)
```

* `D` and `E` become new commits (`D'`, `E'`) with new hashes.
* The old `D` and `E` no longer exist in your visible history.

### Why Use Rebase?

* Keeps project history **linear and clean**.
* Avoids excessive merge commits.
* Makes it easier to review changes and trace history.

### When Not to Use Rebase

**⚠️ Never rebase public/shared branches!**

Do **not** use rebase if:

* The branch has been pushed to a shared remote (e.g., GitHub).
* Other people might be using those commits.

**Why?**
Because rebase rewrites history (commit hashes change), anyone else based on the old commits will run into conflicts and issues.

**Safe rule:**
Use rebase for **local, personal branches** only.
