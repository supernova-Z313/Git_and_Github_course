## Aliases

Git allows you to define **command shortcuts (aliases)** in your global config file, located at `~/.gitconfig`. 
You can create aliases to simplify commonly used commands.
For example, to create shortcuts for `git status` and `git commit -m`, add this to your `.gitconfig` file:

```ini
[alias]
    s  = status
    cm = commit -m
```

Then you can use them like this:

```bash
git s
git cm "My commit message"
```

Git will replace your alias with the full command and pass any arguments in order.

### Useful Alias Resources:

* [Must-have Git aliases (advanced examples)](https://www.durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/)
* [Git aliases gist (by mwhite)](https://gist.github.com/mwhite/6887990)
* [GitAlias community project on GitHub](https://github.com/GitAlias/gitalias)
