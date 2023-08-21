# Rebasing

Rebasing is a powerful feature of Git that allows you to rewrite the history of a branch. When you branch, the commit and branch from which you branched from becomes the base of *your* branch's history. However, if changes are made to the base branch then your branch and the base branch are said to have divergent histories. If you want to integrate the changes from the base into your branch you have two options:

1. Merge the changes into your branch
2. Rebase your branch

Merging is the simplest and most obvious solutions. it involves simply pulling the changes from the base branch back into your branch as an new merge commit, tieing the histories together. This is often what you will want to do but it cna clutter the history of your branch if the base branch is very active as you will often have to merge the base back into your branch.

Rebasing, as the name suggests allows you to rip up the base of your branch and root it to the `HEAD` of the same or even another branch. This allows you to take the changes and apply them into the **history** of your branch.

```sh
git rebase <new-base-branch>
```

## Interactive Rebasing

Git also offers interactive rebasing which allows you to control exactly how the history is rewritten for the branch. This feature can be enhanced by IDE (Integrated Developer Environments) allowing you to effectively rewrite your progress as you go.

```sh
git rebase -i <new-base-branch>
```

## When not to rebase

Rebasing is powerful but can make it difficult to track when upstream/divergent changes are integrated into a branch. In general it is best to ***not*** rebase when the branch is public (ie. rebase `main` onto a feature for... whatever reason) especially if the branch has an upstream remote as this will create divergent histories between your local rebased branch and the remote which can be extremely difficult to fix and track.
