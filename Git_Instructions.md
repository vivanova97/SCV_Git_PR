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
## 16. Synchronize Changes Between a Local and Remote Repository
Pushing and pulling are fundamental Git commands used to synchronize changes between a local and remote repository on GitHub. Here are the steps to push and pull changes using Git:

### Pushing Changes:
1. First, navigate to the local repository on your computer that you want to push to GitHub.
2. Make sure you have committed all changes you want to push using the `git commit` command.
3. Push your changes to GitHub using the `git push` command:
```
git push -u origin <branch name>
```
Replace <branch name> with the name of the branch you want to push. If you are pushing changes to the main branch, you can leave out the branch name.
4. GitHub will prompt you to enter your username and password to authenticate your push. If you have set up SSH authentication, you won't need to enter your password.

### Pulling Changes:
1. First, navigate to the local repository on your computer that you want to pull changes into.
2. Use the `git pull` command to fetch and merge changes from the remote repository:
```
git pull origin <branch name>
```
Replace <branch name> with the name of the branch you want to pull changes from.
3. If there are any conflicts between the local and remote repositories, you'll need to resolve them manually. The `git status` command will show you which files have conflicts.
4. Once you have resolved any conflicts, use the `git add` and `git commit` commands to commit the changes to your local repository.

## 17. Creating Pull Requests
### What is a **pull request**?
A pull request is a feature of Git and GitHub that allows developers to propose changes to a repository hosted on GitHub. It is a way for developers to collaborate and contribute to a project, even if they do not have direct access to the original repository.

When you create a pull request, you are essentially asking the owner(s) of the repository to pull in your changes and merge them into their codebase. Pull requests are commonly used in open source projects to allow contributors to submit their changes and have them reviewed and accepted by the project maintainers.

Pull requests typically include a description of the changes, as well as any relevant discussion or context around the changes. They can also include comments and feedback from other contributors or maintainers.

Once a pull request is submitted, the repository owner or maintainers can review the changes, provide feedback, and decide whether to accept or reject the pull request. If accepted, the changes will be merged into the repository and become a part of the codebase.

### How to create a pull request?
To create a pull request on GitHub, you can follow these steps:
1. Fork the repository you want to contribute to on GitHub. This will create a copy of the repository in your own account.
2. Clone the forked repository to your local machine using the `git clone` command:
```
git clone https://github.com/<your-username>/<repository>.git
```
Replace <your-username> with your GitHub username and <repository> with the name of the repository you forked.
3. Create a new branch for your changes using the `git checkout` command:
```
git checkout -b <branch-name>
```
Replace <branch-name> with a descriptive name for your branch.
4. Make your changes to the code and commit them using the `git add` and `git commit` commands:
```
git add .
git commit -m "A descriptive commit message"
```
5. Push your changes to your forked repository on GitHub using the `git push` command:
```
git push origin <branch-name>
```
6. Go to the original repository on GitHub and click on the "Pull requests" tab.
7. Click on the "New pull request" button.
8. Select the base branch and the compare branch. The base branch is the branch you want to merge your changes into, and the compare branch is the branch containing your changes.
9. Review the changes in the pull request and add a description of the changes if necessary.
10. Click on the "Create pull request" button to submit your pull request.