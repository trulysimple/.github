# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects! :tada:

This guide will walk you through our contribution workflow. (2min read :zap:)

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will _not_ accept PRs that try to change the contribution worfklow itself. :no_entry_sign:

Here is a list of tools that we use in most repositories, that you should know before contributing:

- [Bun](https://bun.sh/docs)
- [changesets](https://github.com/changesets/changesets)
- [CSpell](https://cspell.org/)
- [eslint](https://eslint.org/)
- [Husky](https://typicode.github.io/husky)
- [lint-staged](https://www.npmjs.com/package/lint-staged)
- [Prettier](https://prettier.io/)
- [publint](https://publint.dev/)
- [TypeScript](https://www.typescriptlang.org/)

## Branching

Please open a new issue before you start working, or select an existing one.
When selecting an issue to work on, use the naming convention `issues/<issue_number>` to create your branch.

## Committing

When committing your code, a _pre-commit_ hook will execute at least one of the following steps:

- run unit tests and report coverage
- compile the code for distribution
- lint, format and spell-check the code

If the repository has a `docs` folder or package, make sure to update the documentation, if applicable.

## Submitting

When submitting your changes, a _pre-push_ hook will execute at least one of the following steps:

- verify the branch name
- verify changeset status

Add a changeset to explain how your changes will impact users, and this will appear in the changelog along with an acknowledgement. :sparkles:

## Versioning

Since we use semantic versioning, your changes should be accompanied by an _intent_, which corresponds to a long-lived branch:

| Intent | Base branch | Issue type        | Description |
| ------ | ----------- | ----------------- | ----------- |
| major  | `next`      | feature request   | when you make incompatible API changes                     |
| minor  | `dev`       | feature request   | when you add functionality in a backward compatible manner |
| patch  | `main`      | bug/vulnerability | when you make backward compatible bug fixes (the default)  |

Notice that the `main` branch receives patches most of the time, but eventually receives minor changes and, less frequently, major changes.
Version bumping is handled in an automated way.
