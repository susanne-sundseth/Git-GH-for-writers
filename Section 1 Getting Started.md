# Section 1 Getting Started with Git and GitHub

**Note**: Lessons that are not included are practice exercises.

## Lesson 1 Intro

**Git**: Free, open source version control system. It only stores the differences between versions. The differences are stored in the hidden .git folder in the repo. To view the ,git folder, select **View** > **Show** > **Hidden Items** in File Explorer.

**GitHub**: Commercial platform on which you can host your files remotely and manage them using Git. Git Hub has a good UI and makes collaboration easy. It is free for public files.

## Lesson 2 Docs Like Code

Documentation is treated like code via processes. See _Docs like Code_ by Anne Gentle.

The docs like code method uses:

* Text formats for documentation that are human readable.
    * **Markdown** (.md): Doesn't have tags. Has many variations called flavors, for example, GitHub-flavored markdown (GFM).
    * **reStructuredText** (.rst): Used primarily in the Python programming language community for technical documentation. No tags or flavors, can extend its functionality. More complex than Markdown and harder to read.
    * **Asciidoc** (.adoc or .txt): Similar to reStructuredText with no tags, one flavor, and can extend functionality.
* Version control tools such as Git and GitHub.
* Review processes similar to code reviews.

**GitBook**: Similar to GitHub but specific to documentation. You can use Git with GitBook.

## Lesson 3 Version Control

Also called revision control systems or control source systems.

**Collaboration**: With version control systems, multiple users manage the versions as if the files all had the same name (unlike intro-v1.text, intro-v2.txt, intro-v3.txt, etc.)

### Git Innovations

* Separates commit and push processes: Documents are hosted remotely but worked on locally. You upload when you are ready to share your work.

* Git only stores the differences between versions, not each version in its entirety. Every local computer stores the differences for all versions. On older systems, you only stored what you were working on.

* Git manipulates files using the file system. File content change with _git_ commands. 

### GitHub and similar platforms

You can create a remote repository on any server but commercial platforms make it easier to manage. GitHub is probably the most popular, but others are available and provide other features like better security or better integrations with other tools than GitHub. Examples are BitBucket, GitLab, and Beanstalk.

## Lesson 4 Getting Started with Git

The command line via Git Bash gives you the full power of Git. The GUI is not intuitive. 

Use Notepad++ as your text editor.

> [!IMPORTANT]
> Right-click to cut and paste. You cannot use keyboards shortcuts.

## Lesson 6 Getting Started with GitHub

Multiple users can read and/or write versions, if they have permission to write. Companies often pay to keep their files private but open source files are mostly public.

### Repositories (or repos)

* A repo holds a directory structure (folders) with files.
* It contains all versions and history.
* Typically exists locally and remotely but they not always in sync.

You can create a repo locally and then push it to GitHub but easier to create in GitHub and then clone locally.
* Always include a ReadMe.md file. It is the documentation for the repo.
* After the repo is created in GitHub, click the **<>Code** button to access and copy the URL. You can then use the command below to clone the repo locally. You can also opt to open the repo with GitHub Desktop.

    ```
    git clone https://github.com/<user>/<repo>
    ```
* Confirm that the repo was created in your C drive.

# Lesson 7 GitHub Authorization

GitHub authorization requires a personal access token. See https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens.

# Lesson 9 Command Line

This course uses the Unix operating system command line to use Git.

### Unix commands
* **pwd**: Returns the path of the current directory (print working directory)
* **ls**: Returns list of directories (folders) and files in the current directory
* **mkdir**: Makes new directory but won't change to that directory
* **cd**: Use to move to a different directory
    * **cd _name_** => Specify the name of the directory to change to

        ![screenshot of cd command using path](https://github.com/susanne-sundseth/Git-GH-for-writers.git/assets/cd_directory_name_with_path.png)

    * **cd .** =>  Current directory
    * **cd ..** => Moves one directory up
    * **cd ~** => Moves to the home directory

        (Research why bullet does not render correctly in GitHub; correct in VS Code preview)

### Command Line Shortcuts
* **Tab**: Fills in the rest of the directory name when possible
* **Up arrow**: Scrolls through previous commands

### Command Structure
_command -o --option argument(s)_
* Options modify the command
    * Use one dash for one-letter options

        ```
        git commit -m "Marketing changes"
        ```
    * Use two dashes for multiple letter options
    * A command can contain more than one option
* Arguments are additional data
    * If an argument is comprised of multiple elements that are separated by spaces, put the elements in quotes.

        ```
        git config --global user.name "Anna Hoffman"
        ```
        
## Lesson 11 Git Concepts

### File stages
1. **Unstaged**: A local file was created, modified, or deleted in Git. Keep unstaged if you made changes that you are not sure you want to keep.
2. **Staged**: A local file is marked with the intention to commit (save) in Git. Stage the file when you are fairly certain you want to keep the change.
3. **Committed**: Save the version in Git. Include a description of the change with each commit.
4. **Pushed**: Upload the committed file to GitHub or other server so you can share with others.

### Git Commands for Stages
1. **Unstaged**: No commands. Just save changes to your machine.
2. **Staged**: Use the _git add_ command. You can stage all eligible files or name a specific file.
3. **Committed**: Use the _git commit_ command with a description. All staged files will be committed.
4. **Pushed**: Use the _git push_ command. All committed files that were not previously pushed are pushed.

### Text Versus Binary Files
* Git works on both text and binary (images, video, audio, etc) files.
* Git can reliably merge text files but not binary files.


















