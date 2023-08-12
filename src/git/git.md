# About

## What is Version Control?

Version Control allows for changes within a repository to be tracked. This allows for you to retain a historical ledger of your source code. This allows you easier move between different points in your repository's history. It also allows you to develop features on separate branches so the changes do not affect the currently working codebase

## What is Git?

Git is a Source Control Management tool (SCM). It keeps a history of multiple files and directories in a bundle called a repository. Git tracks changes using save points called commits. Commits use .diff files to track the difference in files between commits. Repositories can have multiple branches allow many different developers to create new changes and fixes to a codebase that are separate from each other. You can also switch between branches to work on many different changes at once. These branches can then later be merged back together to a main branch, integrating the various changes.

### Common Terms in Git

- Repository - A project, workspace or folder containing your codebase.
- Staging - State the files that are to be added, those that have changed or those that have been deleted from repository for a commit.
- Commit - A saved snapshot of the codebase that has an associated hash.
- Branch - A separate history chain that can later be merged into other branches.
- Clone - A machine local copy of a repository, usually obtained from a remote repository hosting service (GitHub, GitLab).
- HEAD - The top (most recent) commit of a branch or repository.
- Checkout - The means to switch to a branch (HEAD) or commit.
- Pull/Push - Sync local repository with remote repository by pushing your changes your pulling the remote ones.
- Fetch - Pull metadata about for remote changes without integrating remote changes.
- Merge - Combine the history of another branch into the current branch.
- Stash - Save changes in a temporary save commit as a Work-In-Progress (WIP).
- Tags - A named commit in a repository's history.
- Rebase - A technique for reapplying commits on top of a base branch HEAD.
- Diff - The difference between a file, folder, commit or branch across commits and branches.
- Remote -  A copy of a repository that lives off machine.

### Git Workflow

The basic workflow for getting started with  are as follows:

1. Initialise a repository [Create]
2. Add/write file contents
3. Stage changes
4. Commit changes
5. Create branches for different features, usually branched from the `main` branch (or equivalent)
6. Add/make changes
7. Stage new changes
8. Commit changes
9. Repeat 6-8 until feature is done
10. Create a 'Pull Request'. This is a request for the owner of the `main` branch to merge your branches changes into `main` ie. pull them into main.
11. Code owner merges feature branch into `main`
12. Deploy changes
13. Repeat 5-12 for projects lifetime.