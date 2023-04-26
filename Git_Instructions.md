![Git_Github Logo](Git_Github.png)

# Instructions for Working With Git and GitHub
## 1. Check if Git is installed 
In your terminal, use command `git --version`. 
If Git is installed, information with the version of the program will appear. 
If it is not installed, an error message will appear.

## 2. Install Git
Download the last version of Git from https://git-scm.com/downloads.
Install with default settings.

## 3. Git Setup
When using Git for the first time, you need to introduce yourself.
To do this, use the following commands:
```
git config --global user.name Your Name
git config --global user.email your_email@example.com
```
## 4. Initializing a Repository
Create a directory for the project. 
Go to the new directory via your terminal.
In the terminal, type in command `git init`.  
Next, type command `git add .` to add the files to the next commit.
Finally, type `git commit -am "your comment"`.
Congratulations, changes to your directory are now being tracked by Git!

## 5. Saving Changes Made to Repository
Use the command `git add file_name` to add file changes to the next commit. 
If you have several files that you want to add to the commit, you may use the command `git add .` to stage all files.
After the `git add` command, you must create a commit to affix the changes. To do this, use `git commit -m "your comment"`.
These two commands may be combined into one. To combine `git add .` and `git commit` into one command use 
`git commit -am "your comment" `.  To see the difference between the current file and the last commit (or in other words to see the changes
that need to be staged ) use `git diff`.
To see which files have changes that are staged for the next commit use `git status`.
## 6. Viewing Your Commit History
To view all the commits you made previously you may use `git log`. 
This command will show the hash, author, date, and comment for each commit.
To view the shortened version of commit history, use `git log --oneline`. This command will show just the hash of the commit and the comment associated with it.
If you want to view just the last two commits, you may use `git log --oneline -2`.
You may also view the changes made within each commit by using `git log --oneline -p`.

## 7. Moving Between the Commits
You may visit each commit to see what the file looked like at the time of the commit. To do this, use the `git switch` or the `git checkout` command followed by the desired commit's hash. 
The hash is a combination of symbols that helps identify the commit and can be found using the `git log` command. The first four symbols are enough for git switch and git checkout to locate the commit. 
To continue working on your file, you must return to the latest commit by using either `git switch -` or `git checkout master`.
