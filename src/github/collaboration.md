# Collaborating

While GitHub can simply be used as a remote host for repos, allowing you to push and pull to and from a central location, the platform has many more features for allowing teams of people to collaborate on many different kinds of codebases and coordinate development with people from across the world.

## GitHub flavoured Markdown

A large proportion of text written on GitHub is written in Markdown (like this books source). Markdown is a markup language which can be used to describe the format and structure of written text, similar to HTML or LaTeX. There are many variations of Markdown which add various functionality to the language. GitHub uses its own version which extends the capabilities expressed in the CommonMark (standard) Markdown specification.

- [CommonMark](https://commonmark.org/)
- [Markdown Basic Syntax Guide](https://www.markdownguide.org/basic-syntax/)
- [Markdown Extended Syntax Guide](https://www.markdownguide.org/extended-syntax/)
- [GitHub Flavoured Markdown (GFM) Specification](https://github.github.com/gfm/)

GitHub's extensions to Markdown include some common extensions found across many Markdown parsers including support for Strikethrough text, tables and task list items (checklist). These allow you to express more complex structures with Markdown however are not that interesting and specific to GitHub. You can see the syntax for most of Markdown in the second and third links above including these common extensions.

More interesting are the collaboration based extensions to Markdown that are specific to GitHub. Within any Markdown text on GitHub you are able to link and refer to Issues, discussions, Pull Requests (PR), commits, people and even organisation teams from any repo/org. This is done by using the characters `#` and `@` as prefixes.

### Prefix - `#`

You may notice that Issues, PRs and discussions have an associated #-number. This is used to reference the item within other items of the same or other repos. The `#` prefix can be used to create a link to the item in the Markdown of the current item. The Markdown editors on GitHub will even render a scrollable UI component you can use to search by name for the item you want to link when you type start typing `#`. You can even reference items from different repos (as long as they are public) by prefixing the `#` with the name of the owner (GitHub username) and the repos name eg. `MonashDeepNeuron\HPC-Training#1`. You can also create a pretty link if you put the link somewhere in a list item.

### Prefix - `@`

Like many social media platforms, the `@` prefix is used to mention users and teams with a users handle being their username. Like `#`, typing `@` will bring up a list of users and teams you can mention, autocompleting the text if you select an option manually. Teams from organisation are prefixed with the orgs name (like cross repo item links) followed by the team name. eg. The Monash DeepNeuron GitHub organisation has a GitHub team called 'HPC Training' which can be mentioned like so `@MonashDeepNeuron/hpc-training`. Mentioning a GitHub team notify the whole team. You can also use the `@` prefix to link specific commits however, no matter which repo it is from you must prefix the whole thing with the repo owner and name eg. `MonashDeepNeuron/HPC-Training@767c7f0`.

> Note: Team names can have spaces but in links the spaces are replaced with dashes/hyphens (`-`).

## Collaboration Guidelines and Documents

Within a repo there are often many common documents that are used to describe the collaboration process and guidelines for an OSS. These documents are used to outline the behaviour expected by contributors, how to make contributions, often the codes styling guidelines etc.. Here are some common documents you may find in a repo and the overarching purpose they serve to contributors and users.

> Note:
>
> - Really any kind of file can be used to store this as long as the text is accessible by users and contributors so often plain text files (`*.txt`) or Markdown files (`*.md`) are used. Markdown is often favoured as it has better facilities to describes the structure of the document and can then be rendered on GitHub or externally.
> - It is a convention that this contributor documentation files be capitialised however, it is not required.
> - None of these documents are strictly necessary for a repo to function however, they can make it easier for peopel to start contributing to one.

- README - This is the front page of your codebase. Often containing a summary of the project, a 'quickstart' tutorial and may some examples (all optional).
- CONTRIBUTING - Describes the steps potential contributors should take to make contributions to the project.
- CODE_OF_CONDUCT - The expected behaviour of contributors when interacting with each other and users.
- GUIDELINES - Similar and like a combination of the CODE_OF_CONDUCT and the CONTRIBUTING documents.
- LICENSE - Details the license the code operate under and
- INSTALL - Instructions on how to install, setup and use a project either for development or end-user usage.
- CITATION - If your work is academic in nature you can use this file to hold the appropriate citation so users of the project or people that took inspiration of the project can properly cite your work (often uses the `*.cff` extension).
- ACKNOWLEDGMENTS / AUTHORS - A file listing the contributors, authors, co-authors, owners and/or co-owners of a repository. Can also be used to pay tribute to people who've helped with the project, particularly if the contributions were indirect or undocumented (advice etc.).
- CHANGELOG - Used to describe the changes between one version to another. Many of these files could be littered throughout your project if it has many independent parts or has had a long lifetime.
