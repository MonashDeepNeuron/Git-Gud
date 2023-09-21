# Merging

Merging is the process of combining two (or more) histories together. The commits of the branch being merged into another are 'replayed' onto the 'base' branch synchronizing the histories and finally combining the result into a single commit. Merging two branches requires the branches have a common ancestor commit that can be used as the base of the combined histories. To merge branches we use the `merge` command, supplying the name of the branch we want to merge, which will be merged into the the current branch.

```sh
# Merge branch 'feature' into this branch
git merge feature
```

## Dealing with Merge Conflicts

Conflicts occur when Git cannot automatically merge two branches together. When this occurs, you will have to manually intervene and decide which changes you want to keep. When you have resolved the conflicts you then stage and commit them in a new commit as you would any other set of changes.

### Conflict Makers

Git uses conflict markers in your source to indicate the difference between your local changes and the changes you are integrating in. These markers are:

- `<<<<<<<` - Indicates the start of your local difference.
- `=======` - The separator (ie. start) between the local and external difference.
- `>>>>>>>` - Indicates the end of the external difference.
