# Branches, Stashes and Tags

Git has various ways of storing and marking the different states and histories of a repo. The most common is a _branch_, which serves as a logically separate history for a repository. This allows various changes from multiple people to not conflict with each other. _Stashes_ are temporary stores of changes that can be pushed to or popped from, kind of like a stack of changes. _Tags_ are named markers for commits in a repo's history.

## Branches

To create a new branch, you simply use the `git branch` with the name of the branch as the argument. This will create a new branch `HEAD` at the commit you are currently at. You can also pass a commit hash as a second argument to create the branch at that associated commit. Renaming a branch can be achieved by using the `-m` or `-M` (forced) flags and passing the old name (optional) and new name as arguments respectively. You can also delete branches using the `-d` flag. To switch to a branch we use the `checkout` command, supplying the branch name as an argument.

```sh
# Create a new branch
git branch new-branch

# Switch to the new branch
git checkout new-branch

# Rename the current branch
git branch -M new-branch-2

# Switch back to the main branch
git checkout main

# Delete the previously created branch
git branch -d new-branch-2
```

> Note: You can create a new branch and switch to it using the `-b` flag with the `checkout` command.
>
> ```sh
> git checkout -b new-branch
> ```

## Stashes

Stashes store WIP changes that can be reapplied on to the currently checked out commit. Stashes are labelled by a number value starting at 0, indicating the most recent stash. You can `pop` or `drop` (delete) a stash from a particular index by providing it as an argument, with the default being the most recent stash. You can also list a repo's stashes using the `list` sub-command.

```sh
# Create a stash
git stash

# Pop the most recent stash
git stash pop

# Drop (delete) the most recent stash
git stash drop

# Stash with a message
git stash -m "Stash 1"
# Some changes
git stash -m "Stash 2"
# Some changes
git stash -m "Stash 3"

# List stashes
git stash list
stash@{0}: On main: Stash 3
stash@{1}: On main: Stash 2
stash@{2}: On main: Stash 1
stash@{3}: WIP on main: cea4a92 current HEAD commit message

git stash pop 1

git stash list
stash@{0}: On main: Stash 3
stash@{1}: On main: Stash 1
stash@{2}: WIP on main: cea4a92 current HEAD commit message

git stash drop 1

git stash list
stash@{0}: On main: Stash 3
stash@{1}: WIP on main: cea4a92 current HEAD commit message
```

## Tags

Tags allow us to name a particular commit such that it can be referenced and changed to it. Tagging is mostly used to mark certain versions of a codebase. Tags can be created using the `tag` command and providing a label for the tag. Like most of Git, the `-d` flag can be used to delete a tag as well.

```sh
# Create tag
git tag v1.0.0

# List tags
git tag
v1.0.0

# Delete tag
git tag -d v1.0.0
```
