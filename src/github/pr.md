# Pull Requests

Pull Requests (PRs) are requests from collaborators to pull in their new changes from a feature branch into one of the main development, testing or deployment branches. This allows the maintainers of a project to more carefully view the changes made and consider how they want the changes to be integrated. Maintainers and reviewers can also request the contributor to make changes to their contribution to make it fit better with the existing codebase. PRs are essential to quality assurance (QA) and ensuring that breaking changes are not introduced to a codebase unless explicitly allowed. A PR is essentially just a call to `git merge` with extra steps and oversight of the merge although a squash merge or rebase can be chosen instead. PRs can also be created as drafts, allowing you to continue to commit changes to the incoming branch without the risk of maintainers or other contributors completing the PR before it is ready.

> Note: A squash merge will combine the history of all commits on the incoming branch into a single commit that is then added to the base branch.

## Discussion Thread

Just like Issues, PRs also have a discussion thread that allows conversations about the PR to be in the same place as the PR.

## Closing a PR

Again, like Issues, you can close a PR meaning it cannot be merged without reopening the PR.

## Reviewers

This section allows for you to assign people you wish to review the changes. Many PRs are required to have at least one approved review for a PR to go through. Reviews look at the diff of the changes and can add comments as specific to a line or to an entire file or for the whole PR. Reviews can request that changes be made, blocking the PR until it has been resolved.

## Assignees

Assignees allow you to add a person you want to work on merging a particular PR.

## Labels

Labels are descriptor tags that can make it easier to categorise PRs which can make it easier to find or group common PRs together.

## Projects

This section allows you to add your PR to a project board and have it tracked by GitHub automatically allowing better integration between a repo's PRs and the general management of the team or organisation.

## Milestones

You can make a PR a part of a milestone's progress.

## Development

This section shows the Issues that are linked to the PR. Issues can be linked by creating the branch from the Issue or by using ['Closing Keywords'](https://docs.github.com/en/Issues/tracking-your-work-with-Issues/linking-a-pull-request-to-an-Issue) in the description of the PR.

## Notifications

Change your notification settings for the PR.

## Participants

View who is/has been involved in a PR.

## Lock conversations

Lock the conversation from further modifications (usually for archival purposes).
