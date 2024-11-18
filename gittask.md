# PART 1 Git Basics

### Task 1: Install and Configure Git

1. Install Git from  [git-scm.com](https://git-scm.com/downloads).


2. Configure Git with your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

```
These commands tell Git your name and email. This information will be added to every commit you make, so others know who made the changes.

3.Verify your Git configuration

Use git config --list to verify your configuration.

### Task 2: Initialize a Repository

1. Create a new folder for your project and navigate to it:

```bash
mkdir git_task_list2
cd git_task_list2
```
Purpose : Initialize a .git folder to track changes to your files.

_____

# Part 2 : Git Workflow

### Task 3: Create a File and Make Multiple Commits

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

### Task 4: Check Status and Log

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

### Task 6 : Branch Management

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

### Task 7 : Merging Branches

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

### Task 9 : Remote setup
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

Output would be:
```bash
origin  https://github.com/Hardagya12/salesforce-clone.git (fetch)

origin  https://github.com/Hardagya12/salesforce-clone.git (push)
```
### Task 10 : Pushing and Pulling Changes

1. Push changes to the remote repository:

```bash
git push origin feature-enhanced
```

This command pushes the changes in the main branch to the remote repository.

2. Pull changes from the remote repository:

```bash
git pull origin feature-enhanced
```

This command pulls the changes from the remote repository and merges them into the main branch.

### Task 11 : Cloning a Repository

1. Clone a remote repository:
``` bash
git clone https://github.com/Hardagya12/salesforce-clone.git
```
This command clones the remote repository and creates a local copy of it.

# Part 5 Advanced Git
### Task 12 : Stashing Changes

1. Save uncommitted changes

```bash
git stash
```
This command saves the uncommitted changes in a temporary stash.

2. Apply saved changes

```bash
git stash apply
```
This command applies the saved changes to the current branch.

3. Drop the stash

```bash
git stash drop
```
This command drops the temporary stash.

### Task 13 : tagging Commits

1. Create a tag and annote it

```bash
git tag -a v1.0 -m "Version 1.0"
```
This command creates a tag named v1.0 and annotates it with the message "Version 1.0".

2. List all the tags

```bash
git tag
``` 
3.Push the tag to the remote repository 

```bash
git push origin v1.0
```

### Task 14 : Rewriting Commit History

1.Use interactive rebase to modify commit messages

```bash
git rebase -i HEAD~3
```
This command starts an interactive rebase session, allowing you to modify the commit messages.

### Task 15 : Cherrypicking Commits

1.Apply a specific commit to another branch

```bash 
git cherry-pick <commit-hash>
```
This command applies a specific commit to the current branch.

# Part 6 : Collaboration

### Task 16 : Forking and Pull Requests

1. Fork a repository and cone locally

```bash
git clone https://github.com/Hardagya12/salesforce-clone.git
```
This command clones the remote repository and creates a local copy of it.

2. Make changes and push them

```bash 
git checkout -b fix-typo
echo "Typo fixed" >> README.md
git commit -m "Fixed a typo"
git push origin fix-typo
```
This command creates a new branch named fix-typo and pushes the changes to the remote repository.


3. Open a pull request on GitHub

### Task 17 : Simulating Team Collaboration

1.Simulate a conflict by having two users modify the same file

```bash
git checkout -b feature-enhanced
echo "Feature added" >> file1.txt
git commit -m "Added feature"

git checkout main
echo "Bug fixed" >> file1.txt
git commit -m "Fixed a bug"
```
2. Practice resolving conflicts as a teeam

---

# Part 7 : Ignoring Files

### Task 18 : Using .gitignore

1. Create a .gitignore file

```bash
echo "node_modules" > .gitignore
git add .gitignore
git commit -m "Added .gitignore"
```
This command creates a .gitignore file and adds it to the staging area.