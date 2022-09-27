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

1. **Compared Files**
	
	> diff --git a/rainbow.txt b/rainbow.txt
	
	For each comparison, Git explains which files it is comparing. Usually this is two versions of the same file.
	Git also declares one file as "A" and the other as "B".



2. **File Metadata**

	> index 72d1d5a..f2c8117 100644
		
	The first two numbers are the hashes of the two files being compared.  The last number is an internal file mode identifier.
	


3. **Markers**

	> --- a/rainbow.txt
	
	> +++ b/rainbow.txt

	File A and File B are each assigned a symbol.
	- File A gets a minus sign (-)
	- File B gets a plus sign (+)
	

4. **Chunks**

	> @@ -3,4 +3,5 @@ orange
	
	> yellow
	
	> green
	
	> blue 
	
	> -purple
	
	> +indigo
	
	> +violet

	A diff won't show the entire contents of a file, but instead only shows portions or "chunks" that were modified.
	A chunk also includes some unchanged lines before and after a change to provide some context.



* Chunk Header

	Each chunk starts with a chunk header, found between @@ and @@.
	From file a, 4 lines are extracted starting from line 3.
	From file b, 5 lines are extracted starting from line 3
	
	> @@ -3,4 +3,5 @@
	
* Changes

	Every line that changed between the two files is marked with either a + or - symbol.
	lines that begin with - come from file A.
	lines that begin with + come from file B.
	
	> yellow
	
	> green
	
	> blue 
	
	> -purple
	
	> +indigo
 	
 	> +violet


> Note: + sign does not indicate addition and only indicates changes from the second file and can indicate deletion of the contents of a line.
