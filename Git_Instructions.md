![Git_Github Logo](Images/Git_Github.png)

# Instructions for Working With Git and GitHub
## 1. Check if Git is Installed 
In your terminal, use command `git --version`. 
If Git is installed, information with the version of the program will appear. 
If it is not installed, you will get an error message.

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
Go to the project directory via your terminal.
In the terminal, type in the command `git init`.
Congratulations, changes to your directory will now be tracked by Git!

## 5. Saving Changes Made to Repository
Use the command `git add <filename>` to add a file's changes to the next commit. 
If you have several files that you want to add to the commit, you may use the command `git add .` to stage all files.
After you have staged the changes using git add, you can use the **git commit** command to commit them to the repository. For example, you can use the command `git commit -m "your comment"` to create a new commit with a commit message. 

**git add** and **git commit** may be combined into one command. To combine them use 
`git commit -am <your comment> `.  

To see the difference between the current file and the last commit (or in other words to see the changes
that need to be staged ) use `git diff`.
To see which files have changes that are staged for the next commit use `git status`.
## 6. Viewing Your Commit History
To view all the commits you previously made you may use `git log`. 
This command will show the hash, author, date, and comment for each commit.
To view the shortened version of commit history, use `git log --oneline`. This command will show just the hash of the commit and the comment associated with it.

If you want to view just the last two commits, you may use `git log --oneline -2`. 
You may also view the changes made within each commit by using `git log --oneline -p`.

## 7. Moving Between the Commits
You may visit each commit to see what the file looked like at the time of the commit. To do this, use the `git switch` or the `git checkout` command followed by the desired commit's hash. 
The hash is a combination of symbols that helps identify the commit and can be found using the `git log` command. The first four symbols are enough for git switch and git checkout to locate the commit. 

To continue working on your file, you must return to the latest commit by using either `git switch -` or `git checkout master`.

## 8. Ignoring Files
A **.gitignore** file is used to tell Git which files or directories it should ignore and not track changes for.

Git is a version control system that helps manage changes to files and directories over time. Sometimes, however, there are files or directories in a project that you don't want Git to track, such as temporary files, log files, build artifacts, or sensitive data like passwords or API keys.

By adding these files or directories to the .gitignore file, you can tell Git to ignore them and not include them in the commit history. This helps keep your repository clean and prevents unnecessary clutter and conflicts.

You may add a .gitignore file to your project using the interface of your preferred IDE (Visual Studio Code, PyCharm, etc.) or your terminal. To create a .gitignore file though your terminal, navigate to your project directory via the terminal and use `touch .gitignore`. 

To add files or directories to your .gitignore file type `echo filename >> .gitignore`.

## 9. Creating Branches
To create a new branch:
1. Make sure you're in the branch you want to create the new branch from. You can use the `git branch` command to see which branch you're currently on. The branch with an asterisk (*) next to its name is the branch you're currently on.

2. Use the git branch command followed by the name of the new branch to create the new branch. For example, to create a new branch named "feature-branch", use the command: `git branch feature-branch`

3. Switch to the new branch using the git checkout command followed by the name of the new branch. For example, to switch to the "feature-branch" branch, use the command: `git checkout feature-branch`

Alternatively, you can use the git checkout command with the -b option to create and switch to the new branch in a single command. For example, to create and switch to a new branch named "feature-branch" in one step, use the command: 
```
git checkout -b feature-branch
```

After creating the new branch, you can make changes to the files in your working directory, stage them using git add, and commit them using git commit. These changes will be recorded in the new branch you just created.

To quickly visualize the relationships between the different branches and commits in the repository use the following command :
```
git log --oneline --graph
```


## 10. Merging and Resolving Conflicts
In Git, merging is the process of combining changes from one branch into another. To merge a branch into another branch:

1. Make sure you're in the branch you want to merge the changes into. You can use the git branch command to see which branch you're currently on, and the git checkout command to switch to the branch you want to merge into.

2. Use the git merge command followed by the name of the branch you want to merge into the current branch. For example, to merge a branch named "feature-branch" into the current branch, use the command: `git merge feature-branch`

3. Git will merge the changes from the other branch into the current branch. If there are any conflicts, Git will tell you and ask you to resolve them manually. You can use a text editor to open the conflicting files.
Look for the merge conflict markers (<<<<<<<, =======, and >>>>>>>) in the file, and edit the file to resolve the conflicts.

4. After resolving any conflicts, stage the changes using git add and commit them using git commit.

## 11. Deleting Branches
1. **To delete a merged branch:** Use the git *branch -d* command followed by the name of the branch you merged in to delete the merged branch if it's no longer needed. For example, to delete a branch named "feature-branch" after it has been merged into the current branch, use the command: 
```
git branch -d feature-branch
```
2. **To delete a branch that has not been merged:** Use the *git branch -D* command followed by the name of the branch.  For example, 
```
git branch -D feature-branch
```

## 12. Creating an Account on Github
To create an account on GitHub, you can follow these steps:

1. Go to the GitHub homepage at https://github.com.

2. Click on the "Sign up" button in the upper right corner of the page.

3. Enter your desired username, email address, and password in the fields provided.

4. Choose a plan. GitHub offers a free plan for individual users and small teams, as well as paid plans for larger teams and enterprises.

5. Complete the registration process by following the prompts. You may be asked to verify your email address and provide additional information about yourself.

Once your account is created, you can set up your profile by adding a profile picture, bio, and other details. You can also start creating repositories and collaborating with others on GitHub.

## 13. Creating a Remote Repository
To create a remote repository on GitHub, you can follow these steps:

1. Log in to your GitHub account.

2. Click on the "+" sign in the top right corner of the page and select "New repository" from the drop-down menu.

3. In the "Create a new repository" page, enter a name for your repository. This should be a short, descriptive name that indicates the purpose of your repository.

4. (Optional) Enter a description for your repository. This can be a longer description that provides more information about your repository.

5. Choose whether you want your repository to be public or private. Public repositories are visible to everyone on GitHub, while private repositories are only visible to you and any collaborators you add.

6. (Optional) Choose to initialize your repository with a README, license, or .gitignore file. A README is a file that provides information about your project, while a license and .gitignore file can help you manage your code and protect your intellectual property.

7. Click on the "Create repository" button to create your new repository.

That's it! You have now created a remote repository on GitHub. 

## 14. After Creating Remote Repository: Next Steps
After creating a remote repository on Github, you can either:
1. **Create a new repository** on the command line and tie it to the remote repository:
```
echo "# seminar3" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/vivanova97/seminar3.git
git push -u origin main
```
2. Or, **tie an existing repository** from the command line:
```
git remote add origin https://github.com/vivanova97/seminar3.git
git branch -M main
git push -u origin main
```



