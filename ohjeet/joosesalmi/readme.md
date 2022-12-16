![alt](/github.jpg)

Git työhakemiston kytkeminen GitHub ympäristöön.
----
1. Create a new repository on GitHub.com. 
2. Open Git Bash.
3. Change the current working directory to your local project.
4. Use the `innit` command to initialize the local directory as a Git repository. 
By default, the initial branch is called master.
``` 
$ git init -b main 
```
5. Add the files in your new local repository. 
This stages them for the first commit.
```
$ git add .
```
6. Commit the files that you've staged in your local repository.
```
$ git commit -m "First commit"
```
7. At the top of your repository on GitHub.com's Quick Setup page, click to copy the remote repository URL.
8. In the Command prompt, add the URL for the remote repository where your local repository will be pushed.
```
$ git remote add origin <REMOTE_URL>
# Sets the new remote
$ git remote -v
# Verifies the new remote URL
```
9. Push the changes in your local repository to GitHub.com.
```
$ git push origin main
```
<br>

Git peruskomennot
----
Add

`git add [file]`: Adds a file to the staging area

Commit

`git commit -m "[commit message]"`: Records the file permanently to the version history. 

`git commit -a`: Commits any files you’ve added with the git add command and any files you’ve changed since then.

Status

`git status`: Lists all files that have to be committed.

Log

`git log`: The git log command shows a list of all the commits made to a repository

Push

`git push [variable name] [branch]`: Sends the branch commits to your remote repository.

Branch

`git branch`: Lists all the local branches in the current repository.

Checkout

`git checkout [branch name]`: Is used to switch from a branch to another.

Revert

`git revert <commit>`: Reverses the changes created by the commit.

Reset

`git reset [file]`: Unstages the file, but peserves the file contents.

`git reset [commit]`: Undoes all the commits after the specified commit and preserves the changes locally.

`git reset –hard [commit]`: Discards all history and goes back to the specified commit.
