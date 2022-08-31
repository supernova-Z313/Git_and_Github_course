<h1 align="center">Part 4</h1>

<h3>Ignoring Files</h3>

We can tell Git which files and directories to ignore in a given repository, using a *.gitignore* file.
This is useful for files you know you NEVER want to commit, including:

- Secrets, API keys, credentials, etc.
- Operating System files (.DS_Store on Mac)
- Log files
- Dependencies & packages

Create a file called **.gitignore** in the root of a repository.  Inside the file, we can write patterns to tell Git which files & folders to ignore:

- filename will ignore file
- .DS_Store will ignore files named .DS_Store
- folderName/ will ignore an entire directory
- *.log will ignore any files with the .log extension

for more we can see [this](https://www.toptal.com/developers/gitignore) link or read the refernce.

