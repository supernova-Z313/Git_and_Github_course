## Tags

Tags are used to mark **specific points in a project's history**, commonly for version releases.

There are two types of tags:

* **Lightweight tags:**
  A simple name/label that points to a commit.
  It’s essentially like a branch that doesn't move.

* **Annotated tags:**
  Stores extra metadata such as:

  * Author’s name and email
  * Tag message
  * Date and time

**Annotated tags are more commonly used for versioning.**

### Common Commands:

```bash
# List all tags
git tag

# Filter tags by pattern
git tag -l "v17*"

# Checkout a tag (detached HEAD)
git checkout <tag-name>

# Compare differences between two tags
git diff v17.0.0 v17.0.1

# Create a lightweight tag
git tag <tag-name>

# Create an annotated tag (opens editor for message)
git tag -a <tag-name>

# Show metadata for an annotated tag
git show <tag-name>

# Tag a previous commit
git tag <tag-name> <commit-hash>

# Delete a tag locally
git tag -d <tag-name>
```

### Pushing Tags

By default, **tags are not pushed to GitHub** when you push commits.

To push:

```bash
# Push all tags
git push <remote> --tags

# Push a single tag
git push <remote> <tag-name>
```

---

### 📌 Semantic Versioning (SemVer)

A standard version naming convention:
`major.minor.patch` → example: `2.4.1`

| Part      | Meaning                                                    | Note                           |
| :-------- | :--------------------------------------------------------- | :----------------------------- |
| **Major** | Significant changes that break backward compatibility      | Resets **minor** and **patch** |
| **Minor** | New features or functionality (backward compatible)        | Resets **patch**               |
| **Patch** | Bug fixes or small changes that don’t affect compatibility |                                |

**The initial version typically starts at `1.0.0`.**
