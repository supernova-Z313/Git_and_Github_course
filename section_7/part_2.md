<h1 align="center">Part 2</h1>

**git diff options**

| Command | Description |
|:-------------:|:---------------:|
| ```git diff``` | git diff lists all the changes in our working directory that are NOT staged for the next commit. |
| ```git diff HEAD``` | git diff HEAD lists all changes in the working tree since your last commit.(staged or not) |
| ```git diff --staged``` ```git diff  --cached``` | git diff  --staged or --cached will list the changes between the staging area and our last commit. |
| ```git diff <file-name> <file-name> ...``` ```git diff HEAD <file-name> ...``` ... | We can view the changes within a specific file by providing git diff with a filename. |
| ```git diff branch1..branch2``` ```git diff branch1 branch2``` | git diff branch1..branch2 will list the changes between the tips of branch1 and branch2. |
| ```git diff commit1..commit2``` ```git diff commit1 commit2``` | To compare two commits, provide git diff with the commit hashes of the commits in question. |
