# Getting started with Git—Summary

## Step One: Create a folder for the project
mkdir snitch-sniffer
cd snitch-sniffer

## Step Two: Create a Git repository for the project
### git-init - Create an empty Git repository or reinitialize an existing one
git init

### Create a .gitignore file for the project, ignoring .DS_Store

touch .gitignore

head .gitignore

> .DS_Store
> ._.DS_Store
> **/.DS_Store
> **/._.DS_Store
 
## Step Three: Add file contents to the index
### git-add - Add file contents to the index

### Add a single file
git add README.md

### Add all files (other than those specified in .gitignore: –
git add --all

### Inspect the working tree status
### git-status - Show the working tree status
git status

### git-commit - Record changes to the repository
git commit -am "add README.md"

### For all files: – 
git add --all

git commit -am 'add json rules and python program'

git commit -am 'finish find function'

git log snitch-sniffer.py

### git-checkout - Switch branches or restore working tree files
git checkout 5fd772a292c019a7cf3012b1156685280d4a7d2d snitch-sniffer.py

git commit -am 'restore find function'

git status

git checkout -b lidar-version

### delete the branch if it didn’t work out
git branch -D lidar-version

