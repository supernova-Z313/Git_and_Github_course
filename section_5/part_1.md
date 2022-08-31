<h1 align="center">Part 1</h1>

<h3>Git Branching</h3>

#

Branches are an essential part of Git!
Think of branches as alternative timelines for a project.
They enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.
If we make changes on one branch, they do not impact the other branches (unless we merge the changes)

#

**The Master Branch**
In git, we are always working on a branch The default branch name is master. It doesn't do anything special or have fancy powers.  It's just like any other branch.
Many people designate the master branch as their "official branch" for their code-base, but that is left to you to decide.

In 2020, *Github* renamed the default branch from **master** to **main**. The default Git branch name is still master, though the Git team is exploring a potential change.

#

**HEAD**
HEAD is simply a pointer that refers to the current "location" in your repository.  It points to a particular branch reference.
So far, HEAD always points to the latest commit you made on the master branch, but soon we'll see that we can move around and HEAD will change!

