# Forks

Forks are a combination of branches and clones of a repo. They allow you to copy a remote repo to another (usually remote) location that is independent of the 'upstream' but still retains a connection to its upstream source. Forks can exist for many reasons. A common one is you wish to extend the functionality of a codebase for your own or your organisation's/company's uses. You may also want to make and test an improvement or extension of the codebase and request the changes be integrated into the upstream source for other users to benefit from the change.

To fork a repository you can simply clone a repository and rename the remote name from `origin` to `upstream` and set the repo to track a different remote location as `origin`. This allows you to sync with the `upstream` remote but collaborate at `origin`. Alternatively, you can use GitHub and select the fork button on a repo's '<> Code' page and have GitHub set up the remote fork for you which can then allow you to simply clone the fork to your local machine to start developing on the fork.

When forking a repository you have to be wary of the software license the original source operates on as this restricts what you are able to do with the forked software and how you are allowed to publish and distribute it.
