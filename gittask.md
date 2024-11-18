# PART 1 Git Basics

## Task 1: Install and Configure Git

1. Install Git from  [git-scm.com](https://git-scm.com/downloads).


2. Configure Git with your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

```
These commands tell Git your name and email. This information will be added to every commit you make, so others know who made the changes.

3.Verify your Git configuration

Use git config --list to verify your configuration.

## Task 2: Initialize a Repository

1. Create a new folder for your project and navigate to it:

```bash
mkdir git_task_list2
cd git_task_list2
```
Purpose : Initialize a .git folder to track changes to your files.

_____

# Part 2 : Git Workflow

## Task 3: Create a File and Make Multiple Commits

1.Create a file and add some content:

```bash
echo "My First Project" > README.md
```

2.Stage the file (tell Git to track it):

```bash
git add README.md
```

3.Commit the file (save the changes):

```bash
git commit -m "Initial commit: Added README.md"
```

## Task 4: Check Status and Log

1.Modify the file
```bash
echo "Git is awesome!" >> file1.txt
```
This command adds the text "Git is awesome!" to the end of the file.

2.Check the current status of your repository:

```bash
git status
git diff
```
git status : This command is used to show the current state of the files in the working directory and staging area.

git diff : This command is used to show the differences between the current state of the files and the last committed state.

### Task 5 : Undoing Changes

1.Unstage a staged file

```bash
git resetfile1.txt
```
This command unstages the file. It means the file will no longer be included in the next commit.

2.Discard uncommitted changes

```bash
git checkout -- file1.txt
```
This command discards any changes made to the file since the last commit.

# Part 3 : Branching and Merging

## Task 6 : Branch Management

1.Create a new branch and switch to it

```bash

git checkout -b feature-branch
```
This command creates a new branch named feature-login and switches to it.

2. List all the branches

```bash
git branch
```
This command lists all the branches in the repository.

3.Rename a branch

```bash
git branch -m feature-branch feature-enhanced
```
This command renames the branch feature-branch to feature-enhanced.

## Task 7 : Merging Branches

1. Merge feature-enhanced into main

```bash
git checkout main
git merge feature-enhanced
```

This command merges the feature-enhanced branch into the main branch.

### Task 8: Handling Merge Conflicts

1. Create two conflicting branches and resolve a commit manually:

```bash
git merge feature-branch
```

2. Resolve the conflict manually:
```bash
git add file1.txt
git commit -m "Resolved conflict"
```

# Part 4 Remote repositories

## Task 9 : Remote setup
1. Add a remote repository:

```bash
git remote add origin https://github.com/Hardagya12/salesforce-clone.git
```

This command adds a remote repository named origin to your local repository. The remote repository is a copy of the original repository on GitHub.

2. Verify the remote repository:

```bash
git remote -v
```

This command displays the remote repositories associated with your local repository.