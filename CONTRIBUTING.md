# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects! :tada:

This guide will walk you through our contribution workflow. (1min read :zap:)

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will not accept PRs that try to change the contribution worfklow itself. :no_entry_sign:

Here is a list of tools that we use in all repositories, that you should know before contributing:

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

When you select an issue to work on, please use the naming convention `issues/<issue_number>` to create your branch.

## Committing

We use a _pre-commit_ hook that should run at least the following steps:

- unit tests with coverage report
- compiling code for distribution
- linting and formatting code
- spell-checking

Additionally, if the repository has a `docs` folder or documentation package,
and your changes need to be documented, make sure to update the documentation.

## Submitting

We use a _pre-push_ hook that should run at least the following steps:

- add changeset

Use it to explain the changes you are making, and this will appear in the changelog along with an acknowledgement. :sparkles:
