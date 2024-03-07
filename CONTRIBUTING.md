# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects!
This guide will walk you through our contribution workflow.

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will not accept PRs that try to change the contribution worfklow itself.

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

## Commiting

We use a pre-commit hook that should run at least the following steps:

- unit tests with coverage report
- compiling code for distribution
- linting and formatting code
- spell-checking

## Submitting

We use a pre-push hook that should run at least the following steps:

- add changeset
