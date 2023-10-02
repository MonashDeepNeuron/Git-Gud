# Creating and Cloning a Remote Repository

Creating and cloning a repository on GitHub is super simple. Simply go to [github.com](https://github.com) and click the green 'New' button on the left panel. This will instruct you on how to create a repository. You will have to give your repo a name, a description (optional) and attach a software license and `README.md`. Additionally, you can have it generate a `.gitignore` for the programming language that the source code of the repo will be written in to prevent commonly ignored files (e.g. executables and binaries) from being committed. This will then generate a very boilerplate repo which you can then clone using the `clone` command via SSH or HTTP.

```sh
# Clone with SSH
git clone git@github.com:<username>/<remote-repo-name>.git

# Clone with HTTP
git clone https://github.com/<username>/<remote-repo-name>.git
```

## Uploading a Repository

Alternatively you can create a repository locally and upload it to GitHub at a later date.

### Upload Empty Repository

If you want to upload a new empty repo you can do so by first creating the empty repo on GitHub followed by these commands to upload it to the new empty remote, replacing the content between the angle brackets (`<>`).

```sh
mkdir my-awesome-project
cd my-awesome-project
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main

# SSH
git remote add origin git@github.com:<username>/<remote-repo-name>.git
# HTTP
git remote add origin https://github.com/<username>/<remote-repo-name>.git

git push -u origin main
```

### Upload Existing Repository

You can also upload an existing and well established project to GitHub by simply adding the new GitHub repo as a new remote location.

```sh
cd my-awesome-project

# SSH
git remote add origin git@github.com:<username>/<remote-repo-name>.git
# HTTP
git remote add origin https://github.com/<username>/<remote-repo-name>.git

git branch -M main
git push -u origin main
```

> Note: A repository can have many remotes. The term `origin` isn't a special command or 'keyword' in Git but rather just the conventional name for the default remote host location for repository. You can replace `origin` with whatever name you like.
