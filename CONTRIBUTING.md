# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects! :tada:

This guide will walk you through our contribution workflow. (1min read :zap:)

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will _not_ accept PRs that try to change the contribution worfklow itself. :no_entry_sign:

Here is a list of tools that we use in most repositories, that you should know before contributing:

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

When committing your code, a _pre-commit_ hook will execute at least the following steps:

- run unit tests and report coverage
- compile the code for distribution
- lint, format and spell-check the code

If the repository has a `docs` folder or package, and your changes need to be documented, make sure to update the documentation accordingly.

## Submitting

When submitting your changes, a _pre-push_ hook will execute at least the following steps:

- verify the branch name
- add a changeset

Use the changeset to explain the changes you are making, and this will appear in the changelog along with an acknowledgement. :sparkles:

## Updating

Once a pull request is submitted, it will automatically receive changes from the base branch when available.
You must then update your local copy and perform any necessary adjustments.
