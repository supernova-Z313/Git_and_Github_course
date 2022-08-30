<h1 align="center">Part 2</h1>

<h3>Basic Git command :</h3>

1.  **git status**
	* git status gives information on the current status of a git repository and its contents.

2.  **git init**
	* Use git init to create a new git repository. Before we can do anything git-related, we must initialize a repo first!
	* This is something you do once per project.  Initialize the repo in the top-level folder containing your project.
	*  Note: *Git Tracks A Directory and All Nested Subdirectories.*
	* 	 WARNING: *DO NOT INIT A REPO INSIDE OF A REPO!*
	*	> To delete a repo, locate the associated *.git* directory and delete it.

3. **git add**
	* Use git add to add specific files to the staging area.  Separate files with spaces to add multiple at once.
	* Use git add . to stage all changes at once.
	* Use git status constantly to verify what changes are staged and not staged!

4. **git commit**
	* Running git commit will commit all staged changes.  It also opens up a text editor and prompts you for a commit message.
	* The -m flag allows us to pass in an inline commit message, rather than launching a text editor.

5. **git log**
	* Will show us all commits history.
	* for exit from log page press *q*

