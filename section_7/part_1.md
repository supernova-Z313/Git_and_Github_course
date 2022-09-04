<h1 align="center">Part 1</h1>


<h3>Comparisons With Git Diff</h3>

We can use the git diff command to `view changes` between commits, branches, files, our working directory, and more!
We often use git diff alongside commands like git status and git log, to get a better picture of a repository and how it has changed over time.

**git diff**

Without additional options, git diff lists all the changes in our working directory that are *NOT staged* for the next commit.

```console
git diff
```

**But what structure does the output of this command follow?**

The output of the *git diff* command consists of parts like the figure below.

```
diff --git a/rainbow.txt b/rainbow.txt
index 72d1d5a..f2c8117 100644
--- a/rainbow.txt
+++ b/rainbow.txt
@@ -3,4 +3,5 @@ orange
 yellow
 green
 blue 
-purple
+indigo
+violet
```

1. *Compared Files*

	For each comparison, Git explains which files it is comparing. Usually this is two versions of the same file.
	Git also declares one file as "A" and the other as "B".

> diff --git a/rainbow.txt b/rainbow.txt

2. *File Metadata*
	
	The first two numbers are the hashes of the two files being compared.  The last number is an internal file mode identifier.
	
> index 72d1d5a..f2c8117 100644

3. 