# Getting started with Git—Summary
## Step One: Create a folder for the project
`mkdir snitch-sniffer`

### Make this the current folder
`cd snitch-sniffer`

## Step Two: Create a Git repository for the project
*git-init* - Create an empty Git repository or reinitialize an existing one

`git init`

### Create a .gitignore file for the project, ignoring .DS_Store
`touch .gitignore`

`head .gitignore`

Appears as: –
```
.DS_Store
._.DS_Store
**/.DS_Store
**/._.DS_Store
```
## Step Three: Add file contents to the index
*git-add* - Add file contents to the index

### Add a single file
`git add README.md`

### Add all files (other than those specified in .gitignore): –
`git add --all`

### Inspect the working tree status
*git-status* - Show the working tree status

`git status`

### Record changes to the repository (repo)
*git-commit* - Record changes to the repository

`git commit -am "add README.md"`

### Re-inspect the working tree status
`git status`  
    
## Step Four: Create a branch
*git-checkout* - Switch branches or restore working tree files

*git checkout -b new-branch*

`git checkout -b revised-version`

### Inspect the branches
*git-branch* - List, create, or delete branches

`git branch`

## Step Five: Edit a file
`nano README.md`    

### (Possibly) re-inspect the working tree status
`git status`

## Step Six: Record changes to the repository (repo)   
`git commit -am "edit README.md"`

### (Possibly) re-inspect the working tree status
`git status`

### (Possibly) inspect changes to the file in this branch
*git-log* - Show commit logs

`git log README.md`

### (Possibly) restore a previous version from the working tree files
`git checkout 5fd772a292c019a7cf3012b1156685280d4a7d2d README.md`

### Commit the restored version to the repo
`git commit -am "restore earler version"`

### (Possibly) re-inspect the working tree status
`git status`

## Step Seven: Switch back to the *main* branch and merge the changes
`git checkout main`

### Confirm we're back in the *main* branch
`git branch`

### Merge the changes in *revised-version* with *main* branch
*git-merge* - Join two or more development histories together

`git merge revised-version`
 





### Or delete the branch if it didn’t work out
`git branch -D new-version`

