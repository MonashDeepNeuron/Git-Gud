# Changes, Staging and Commits

Whenever you make changes to the contents of a repository, this changes will be compared as a diff between the working tree and the `HEAD` of the repositories history. To view which files have changed you can run the `git status` command. Once you are happy with your changes, you can add them to the file index for staging. You can specify certain files you want to keep or using `.` to stage all new changes. Finally you can then commit your changes. Commits are saved snapshots of a repo's state. When you create a commit, a hash value is generated for it, this is used to jump back to the commit using `switch` or `checkout`. Commits also have a short message associated with it to describe the changes made in the commit.

```sh
# Stage all changes in repo
git add .

# Commit changes
git commit -m "Commit message"
```
