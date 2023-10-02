# TL;DR

The section of the book is designed to be a quick reference to some of the most common commands or actions for Git and GitHub.

## Installation

[Download](http://git-scm.com)

## Setup

```sh
# Set the name that is identifiable for credit when reviewing version history
git config --global user.name "github-username"

# Set an Email address that will be associated with each history marker
git config --global user.email "github-email"

# Set automatic command line coloring for Git for easy reviewing
git config --global color.ui auto
```

## Initialisation

```sh
# Initialise a directory as a Git repo
git init

# Clone a repo from the URL
git clone <url>
```

## Staging and Commits

```sh
# Show which files are staged
git status

# Stage file or pattern
git add <file-or-pattern>

# Remove all changes
git reset

# Show diff of changed files
git diff

# Show diff of staged files
git diff --staged

# Commit staged changes w/ message
git commit -m "Your commit message"
```

## Branches

```sh
# List branches (* indicates current branch)
git branch

# Checkout to branch
git checkout <branch>

# Create a new branch
git branch <branch>

# Create new branch and checkout to it
git checkout -b <branch>

# Merge incoming branch into current branch
git merge <incoming-branch>
```

## Inspecting and Compare

```sh
# Show commits from the current branch's history
git log

# Show commits on branch-A not on branch-B
git log <branch-B>..<branch-A>

# Show commits that modified a given file, even across renames
git log --follow <file>

# Show diff of what is in branch-A that is not on branch-B
git diff <branchB>..<branchA>

# Display any Git object in human-readable format
git diff <SHA>
```

## Remotes and Sharing

```sh
# Add Git URL as remote
git remote add <remote> <url>

# Retrieve changes from remote without integrating changes
git fetch <remote>

# Fetch and merge changes from a remote branch into your local branch
git pull <remote>

# Transmit changes from local branch into a remote branch
git push <remote> <branch>

# Set current branch to track branch at remote
git push -u <remote> <branch>

# Merge a remote branch into local branch
git merge <remote-name>/<branch>
```

## Rebasing

```sh
# Apply commits from the current branch on top of the new-base-branch.
git rebase <new-base-branch>

# Interactively apply commits from the current branch on top of the new-base-branch.
git rebase -i <new-base-branch>

# Clear all staged changes and rewrite working tree from the specified commit-hash
git reset --hard <commit-hash>
```

## Stashes

```sh
# Save modified and staged changes in stash
git stash

# Show all stashes in stack-order
git stash list

# Pop stash from top of stash-stack
git stash pop

# Drop stash from top of stash-stack
git stash drop
```
