# Common Git Commands

Git is predominately used through its command line interface (CLI). This means Git operates using a variety of different commands (and even sub-commands, command options for commands). Some of the most commonly used commands and their purpose:

|  Command   |                                      Description                                      |
| :--------: | :-----------------------------------------------------------------------------------: |
|   `init`   |                                Initialise a repository                                |
|  `clone`   |                       Clone repository from remote host at URL                        |
| `checkout` |                             Checkout to branch or commit                              |
|  `branch`  |                                     Create branch                                     |
|   `add`    |                               Add files to commit stage                               |
|  `commit`  |                                 Commit staged changes                                 |
|  `merge`   |                 Merge changes from another branch into current branch                 |
|   `push`   |                           Push changes to remote repository                           |
|   `pull`   |                          Pull changes from remote repository                          |
|  `fetch`   | Pull changes from remote repository without integrating changes into local repository |
|  `rebase`  |                      Reapply commits on top of new branch `HEAD`                      |
|  `status`  |                List the currently modified files and status of remotes                |
|   `tag`    |                      Create or list a tag at the current `HEAD`                       |

There are many more commands within Git's CLI. You can view them and their functionality using Git's Manpage. To access the Manpage run the following commands.

```sh
man git
```
