# Git Commands Guide

This guide provides a clear and concise explanation of commonly used Git commands to help you manage your repositories efficiently.

## Repository Operations

### Clone a Repository

`git clone <url>`
Download a copy of the repository.

### Initialize a Repository

`git init`
Create an empty Git repository or reinitialize an existing one.

### Add a Remote Repository

`git remote add origin <url>`
Add a remote repository to your project.

## Basic Commands

### Add Files

`git add <filename>`
Add a file to the staging area.

### Commit Changes

`git commit -m "message"`
Save changes with a message describing the update.

#### Add and Commit Changes

`git commit -am "message"`
Add all changes to the staging area and commit them with a message.

### Push Changes

`git push`
Upload changes from your local repository to the remote repository.

#### Push to a Specific Remote and Branch

`git push <remoteName> <branchName>`
Push changes to a specified remote and branch.

### Pull Changes

`git pull`
Download the latest changes from the remote repository.

#### Pull from a Specific Remote

`git pull <remoteName>`
Pull changes from a specified remote repository.

## Status and Logs

### Check Status

`git status`
Show the working tree status.

### View Commit Logs

`git log`
Show the commit logs.

## Branch Management

### List Branches

`git branch`
List all local branches.

#### List All Branches

`git branch -a`
List all branches (local and remote).

### Create a New Branch

`git branch <name>`
Create a new branch.

### Rename a Branch

`git branch -m <name>`
Rename the current branch.

### Delete a Branch

`git branch -d <name>`
Delete a branch.

### Create and Switch to a New Branch

`git checkout -b <branchName>`
Create and switch to a new branch.

### Merge Branches

`git merge <branchName>`
Merge the specified branch into the current branch.

## Remote Management

### List Remote Repositories

`git remote -v`
List the remote repositories.

## Configuration

### View Configuration

`git config -l`
List all configuration settings.

### Update Global Configuration

`git config --global <key> <value>`
Update a global configuration setting.

### Unset Global Configuration

`git config --global --unset <key>`
Remove a global configuration setting.

### Edit Global Configuration

`git config --global --edit`
Edit the global configuration file.

### Create Aliases

`git config --global alias.<shortcut> <command>`
Create a shortcut for a command.

## Working with SSH

### Generate SSH Key

`ssh-keygen -t rsa -b 4096 -C "<email>"`
Generate a new SSH key.

### View SSH Key

`cat ~/.ssh/id_rsa.pub`
Display the public SSH key.

### Test SSH Connection

`ssh -T git@github.com`
Test the SSH connection to GitHub.

## Stashing Changes

### List Stashes

`git stash list`
List all stashed changes.

### Save Changes to Stash

`git stash save "<message>"`
Stash changes with a message.

### Apply Latest Stash

`git stash pop`
Apply the latest stash and remove it from the stash list.

### Apply a Specific Stash

`git stash apply stash@{<id>}`
Apply a specific stash without removing it from the stash list.

### Drop Latest Stash

`git stash drop`
Remove the latest stash from the stash list.

### Drop a Specific Stash

`git stash drop stash@{<id>}`
Remove a specific stash from the stash list.

### Show Stash Details

`git stash show`
Show details of the latest stash.

### Clear All Stashes

`git stash clear`
Remove all stashes.

## Resetting and Cleaning

### Reset to a Specific Commit

`git reset --hard <commitId>`
Reset the working directory to a specific commit.

### Reset to Remote Master

`git reset --hard origin/master`
Reset the working directory to the state of the remote master branch.

### Unstage a File

`git reset HEAD <filename>`
Unstage a file while retaining its changes in the working directory.

### Restore a Staged File

`git restore --staged <filename>`
Unstage a file, keeping its changes in the working directory.

### Preview Clean

`git clean -n`
Show which files would be removed by `git clean`.

### Force Clean

`git clean -f`
Remove untracked files from the working directory.

## Tagging

### List Tags

`git tag`
List all tags.

### Create a Tag

`git tag <version>`
Create a new tag.

### Annotate a Tag

`git tag -a <version> -m "<message>"`
Create an annotated tag with a message.

### List Tags with Pattern

`git tag -l "<pattern>"`
List tags matching a pattern.

### Delete a Tag

`git tag -d <version>`
Delete a local tag.

### Push a Tag

`git push origin <tag>`
Push a tag to the remote repository.

### Delete a Remote Tag

`git push origin -d <version>`
Delete a tag from the remote repository.

## Ignoring Files

### .gitignore File

Create a `.gitignore` file to specify files and directories that should be ignored by Git.

```markdown
# Example of .gitignore content

_.log
_.tmp
node_modules/
dist/
```
