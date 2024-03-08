# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects! :tada:

This guide will walk you through our contribution workflow. (2min read :zap:)

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will _not_ accept PRs that try to change the contribution worfklow itself. :no_entry_sign:

Here is a list of tools that we use in most repositories, that you should know before contributing:

- [semver](https://semver.org/)
- [changesets](https://github.com/changesets/changesets)
- [Kodiak](https://kodiakhq.com/docs/quickstart)
- [Husky](https://typicode.github.io/husky)
- [lint-staged](https://github.com/lint-staged/lint-staged)
- [eslint](https://eslint.org/)
- [publint](https://publint.dev/)
- [CSpell](https://cspell.org/)
- [Prettier](https://prettier.io/)
- [Bun](https://bun.sh/docs)

## Branching

When selecting an issue to work on, please use the naming convention `issues/<issue_number>` to create your branch.

## Committing

When committing your code, a _pre-commit_ hook will execute at least one of the following steps:

- run unit tests and report coverage
- compile the code for distribution
- lint, format and spell-check the code

If the repository has a `docs` folder or package, and your changes need to be documented, make sure to update the documentation accordingly.

## Submitting

When submitting your changes, a _pre-push_ hook will execute at least one of the following steps:

- verify the branch name
- add a changeset

Use the changeset to explain the changes you are making, and this will appear in the changelog along with an acknowledgement. :sparkles:

## Versioning

Since we use semantic versioning, your changes should be accompanied by an _intent_, which corresponds to a long-lived branch:

| Intent | Base branch | Description |
| ------ | ----------- | ----------- |
| major  | `major`     | when you make incompatible API changes                     |
| minor  | `minor`     | when you add functionality in a backward compatible manner |
| patch  | `main`      | when you make backward compatible bug fixes (the default)  |

Notice that the `main` branch receives patches most of the time, but eventually receives minor changes and, less frequently, major changes.
Version bumping is handled in an automated way.

## Updating

Once a pull request is submitted, it will automatically receive changes from the base branch when available.
You must then update your local copy and perform any necessary adjustments.
