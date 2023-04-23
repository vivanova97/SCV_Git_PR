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
`git commit -am "your comment" `.
