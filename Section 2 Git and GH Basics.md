# Section 2 Git and GitHub Basics

## Lesson 12 Note About GitHub  
The default branch is now called the main branch. Previously it was called the master branch.

## Lesson 13 Adding to the Repository

**Note**: GitHub assumes that you are using GitHub-flavored markdown (GFM).

### Useful Git Commands

**git status**: Shows status of files in a directory. Untracked files are unstaged files.

![Screenshot of git status command return information](https://github.com/susanne-sundseth/Git-GH-for-writers.git/assets/git_status_return_example.png)

**git add**: Use to stage files.
* **git add _filename_**: Use to stage a specific file.
* **git add .**: Use to stage all files and folders within the current directory.

**git reset HEAD _filename_**: Unstage
**git commit -m "_message_"**: Use to commit all staged files that are not committed. 

**git push --set-upstream origin main**: Use to set the upstream branch for the local branch and push the changes to the remote repository. When you create a new branch locally, Git does not automatically know which remote branch it should be associated with. The _--set-upstream_ option helps to establish this association.

**git push**: Use to upload local commits to the remote repository branch. By default, Git selects the remote repository named origin and the current branch to push. The command syntax is _$ git push remote branch_. If a push is successful, refresh your repo in GitHub to see your commits. 

## Lesson 15 Changing Files

When you change a staged file, the status of the file changes to modified and it is automatically unstaged. Use a _git add_ command to restage it.

## Lesson 17 Renaming and Deleting Files

### Renaming
Renaming a file is a change so the file becomes unstaged. You must then add, commit, and push the renamed file. You can rename a file in File Explorer or you can use _mv old-file-name new-file-name_ to delete the old file and create a new file with the same content as the old file.

### Deleting

You can delete from File Explorer or use _rm filename_, then add, commit, and push directory to update the repo in GitHub.

## Lesson 19 Why Git is Designed with Stages

When would you make changes but not save them to Git?: You might maintain an unstaged file because you are experimenting - maybe trying out a table.

When would you stage but not commit?: Continued editing.

When would you commit but not push?: Not ready to share a file.

## Lesson 20 Version Control: Going Back in Time

Use GitHub to view previous commits. 

![Screenshot of commits button in Github](https://github.com/susanne-sundseth/Git-GH-for-writers.git/assets/access_commits_in_gh.png)

### Head
Git tracks all commits but labels one as HEAD. The HEAD is the last commit in the currently checked out branch. You can move the HEAD label to a different commit. Use the commands below when moving the HEAD designation.

**git log**: Shows your history.

**git log --oneline**: Shows history in abbreviated form; easier to read.

**git checkout _commit_**: Use to assign the HEAD label to an older version. When you use this command, Git modifies the .md file so you'll get a message about reloading the file. Click **Yes**.

**git checkout main**: Sets the current verion (HEAD) to the most recent on the main branch.

Use _git log --oneline_ to view the commits, then use _git checkout commit_ to change the HEAD.

![Screenshot of commands to change HEAD](https://github.com/susanne-sundseth/Git-GH-for-writers.git/assets/change_head_example.png)

> [!WARNING]
> Do not make changes to previous commits. If you want to use info from a previous commit, copy it for use in your most current version.

### Best Practices for Committing
* Commit often; ideally each commit contains just one major change such as added a section, deleted a section, or changed product name.
* Include a clear concise description about the change in the commit command message.










