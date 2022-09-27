<h1 align="center">Part 2</h1>

1. **Fast-Forward**
2.  **merge conflicts**
	In this type of merge, the main branch has made some changes after the sub-branch is separated, which changes may not exist in the sub-branch.
	
	In this type of merge, depending on the changes that happened in the main branch, two situations may occur, but it should be noted that in both of these situations, the result is a new commit created after the last commit of the main branch.
	
	As before, after this merger, the two branches have not disappeared and the changes of each are applied separately only to themselves.
		
	```mermaid
	graph LR
	A[2f5d..] --> B[ee86..]
	B --> F[fb45..]
	X{HEAD} -- master --> F
	B --> C((64fg..))
	C --> D((18fr..))
	Y{HEAD} -- bug-fix --> D
	```
	
	- If the changes made in the main branch do not interfere with the contents of the sub-branch, such as creating a new file (changing the same lines of code in one file or deleting a file that exists in another is a case of interference), it will be automatically managed by *Git* And once a comment is received, it is registered for a new commit.
	
	```mermaid
	graph LR
	A[2f5d..] --> B[ee86..]
	B --> F[fb45..]
	B --> C((64fg..))
	C --> D((18fr..))
	F --> E[54po..]
	D --> E
	X{HEAD} -- master, bug-fix --> E
	```
	
	- But if the changes of two branches interfere with each other, *Git* will return the following error to you.
	
	```cosole 
	CONFLICT (content): Merge conflict in blah.txt
	Automatic merge failed; fix conflicts and then commit the result.
	```

	It also changes the contents of your files to indicate the conflicts that it wants you to resolve.
	```
	<<<<<<< HEAD
	The content from your current HEAD
	=======
	The content from the branch you are trying to merge
	>>>>>>> bug-fix
	```
	
	Whenever you encounter merge conflicts, follow these steps to resolve them:
	- Open up the file(s) with merge conflicts
	- Edit the file(s) to remove the conflicts. Decide which branch's content you want to keep in each conflict.  Or keep the content from both.
	- Remove the conflict **"markers"** in the document
	- Add your changes and then make a commit!
	


> Reminder: After merging the branches, you may want to delete some of them, which you can use the following command.

```console
git branch -d <branch-name>
```

