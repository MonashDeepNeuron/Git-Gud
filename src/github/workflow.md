# Workflow

In this page we are going to explore a potential workflow you can use with Git and GitHub when collaborating with multiple people. No it doesn't have a name, I'm not a marketing guy and it doesn't need one. The focus of this workflow is to allow as-easy-as-possible integration of many different features without breaking the entire system and its deployment by funneling changes down from feature (or patch) branches into staging branches and finally into the main deployment branch.

## Main Deployment Branch

In essence you have a single branch that is used as as the deployment branch. You can of course call ths whatever you want but we'll assume this is the `main` branch. From the `main` you make deployments and use tags to mark releases.

## Development and Staging Branches

You also have a mirroring branch that acts as the source of both new feature branches and the staging area to ensure integrating multiple features do not break each others new functionality or existing functionality. I typically call this `dev` but again, you are free to call it whatever you want. You can also have multiple staging levels if you want more rigorous filtering down of features. The `dev` branch is to be kept up to date with `main`. This should be easy to maintain if you only pull `dev` changes into `main` and don't update `main` directly but you can pull `main` back into `dev` if need be.

## Creating Feature Branches

From the `HEAD` of `dev` new branches are created for feature development. This will ensure that if a separate but new feature is created and pulled into `dev` your new feature can benefit or not have issues later on merging the two histories together. If need be features can obviously be created from any point in `dev` history if you do not want to include branch-base staged changes. When a feature is based off an Issue use the GitHub 'Create branch from Issue'. Ensure to change the base branch to the `dev` branch. You can name these branches whatever you want but the GitHub generated one is good enough.

## Merging Features to Development or Staging Branches

When a feature is ready to be integrated, create a PR from the feature branch into the `dev` branch (or appropriately levelled staging branch if applicable) and request reviews from the relevant people/maintainers. If you are not a maintainer then the reviews/maintainers will do the rest and should keep you updated on the PR's progress and may request clarification or revisions to make the changes fit into the existing/upcoming codebase. In the PR's description it is good to include a brief description/list of the changes you have made as well as link and related Issues, PR's, external resources or anything else relevant to the PR however, consult the CONTRIBUTING, CODE_OF_CONDUCT and GUIDELINES files for the repo to ensure you adhere to the specific repos contributing policies as every repo can be different, even if managed by the same people, company and/or organisation.

## Merging Development or Staging Branches into the Main Deployment Branch

If you are a maintainer of a repo you may have to setup a PR for merging upcoming changes into the `main` branch. If you are maintaining a bigger project then coordinating with other maintainers and contributors about which changes you want to integrate into each release can make it easier to create the PRs and stage as many new changes in `dev` that is feasible so you can thoroughly test how the changes play together. You can make a single release for each PR into `main` or you can do multiple PR's if you have a more structured release schedule. Ensure you also have this PR reviewed by others as it can help catch problems before they hit you main branch. You can also branch the `HEAD` of `main` and merge a test PR into this new branch to do test deployments before pulling `dev` into `main`.

## Notes

This is not a very thorough workflow but is aimed to be as simple as possible while still be effective for teams to collaborate together. This workflow does not govern coding practices, commit conventions nor stop bad code from entering a codebase but can help setup a skeleton for collaboration between multiple people. Maintainers and collaborators should still make use of the Issues, Discussions, Projects etc. to help coordinate and track problems and changes for a repo.
