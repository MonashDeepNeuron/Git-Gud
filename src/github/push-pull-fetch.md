# Push, Pull, Fetch

When interacting with remote repos, there are three key operations you will perform frequently. These are pushing your local changes to a remote repo, pulling and integrating new changes from a remote into your local repo and fetching the metadata of available changes.

## Push

Pushing is the process of uploading our local changes to a remote location. You can also use the `-u` flag to set up a new remote reference if the local branch does not exist on the remote yet.

```sh
git push <remote-name>
git push -u <remote-name> <new-upstream-branch-name>
```

## Pull

Pulling is the process of integrating remote changes into the current branch. Under the hood, `git pull` calls `git fetch`, forwarding all command line arguments from `git pull` to `git fetch`. If the current local branch is simply behind the remote's history the local branch will be fast-forwarded by default. If the branch's histories diverge then either `git rebase` or `git merge` will be run depending on the configuration of Git. This allows you to remain up to date with the remote as you develop locally if multiple other people are working on the same branch.

```sh
git pull <remote-name>
```

## Fetch

Fetching is a very powerful tool. It allows us to pull the updated refs from a remote location without integrating the changes into your local repo meaning that we can view what has changed before our local history is fast-forwarded or merged with the corresponding remote branch.

```sh
git fetch <remote-name>
```
