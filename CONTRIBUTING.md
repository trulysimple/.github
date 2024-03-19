# Contributing guide <!-- omit in toc -->

Thank you for investing your time in contributing to our projects! :tada:

This guide will walk you through our contribution workflow. (2min read :zap:)

## Getting started

We strive to make contribution as easy as possible, but we do impose some opinionated practices and,
as such, will _not_ accept PRs that try to change the contribution worfklow itself. :no_entry_sign:

Here is a list of development tools that we use in most repositories, that you should know before contributing:

[Bun](https://bun.sh/docs),
[changesets](https://github.com/changesets/changesets),
[CSpell](https://cspell.org/),
[eslint](https://eslint.org/),
[Husky](https://typicode.github.io/husky),
[lint-staged](https://www.npmjs.com/package/lint-staged),
[Next.js](https://nextjs.org/),
[Nextra](https://nextra.site/),
[Prettier](https://prettier.io/),
[publint](https://publint.dev/),
[React](https://react.dev/),
[TypeDoc](https://typedoc.org/),
[TypeScript](https://www.typescriptlang.org/)

## Refactoring

We believe that technical debt should be paid as soon as possible, rather than accumulated.
However, we also believe that this kind of change must be treated as having a separate purpose.
That way, it will be easier for us to review the changes and avoid negligence during a review.

In this regard, please pay attention to code which is refactored while you're implementing a new feature or fixing a bug.
You will need to extract this code into a refactoring branch before submitting a PR.

## Branching

Please open a new issue before you start working, or select an existing one.
When selecting an issue to work on, use the following naming convention to create your branches:

- `issues/<issue_number>` - the main issue branch
- `refactor/<issue_number>` - a branch for refactoring. If present, this must be merged first.

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

Notice that the `main` branch receives patches most of the time, but eventually receives minor changes from `dev` and,
less frequently, major changes from `next`. Version bumping is handled in an automated way.

> [!IMPORTANT]
> The `dev` and `next` branches should only be updated with `main` when the latter is in a "clean" state,
> i.e., it was recently released, so there are no pending changesets in it.

