# ts-npm-package-boilerplate
This repo is a template for quickly getting a Typescript npm package up and running.

This example project exports a package for adding and subtract numbers. 

To get started you can delete everything inside the src folder except for index.ts, this is the entry point for the package.

## Tech Stack

- Vite
- Vitest 
- Typescript

It includes test examples using vite test

# COMMANDS
## run build for local dist testing
npm run build

## run tests
npm run test

## check test coverage
npm run coverage

## build npm release package
npm pack

## Dry run the npm release package
npm pack --dry-run

## run eslint 
npm run lint

## run and fix eslint issues found
npm run lint-and-fix

## run prettier on your files
npm run pretty

## clean up the codebase by runnning eslint and prettier
npm run clean-up


## Semantic Release
This project already has semantic-release as a dependecy. To get the full benifits of this all commit messages should be in the format it requires. You can see that in their readme [here](https://github.com/semantic-release/semantic-release)

The next step is for your CI to be setup to use semantic-release. You can read how to do that [here](https://github.com/semantic-release/semantic-release/blob/HEAD/docs/usage/getting-started.md#getting-started)