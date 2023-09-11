# ts-npm-package-boilerplate
This repo is a template for quickly getting a Typescript npm package up and running.

This example project exports a package for adding and subtract numbers. 

To get started you can delete everything inside the src folder except for index.ts, this is the entry point for the package.

> When you are ready to build this package, make sure you search for the phrase 'my-lib' and replace this with the name of your package.

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

# Things to know when publishing your package to github.

1. Set up your repository url inside your package.json set up correctly. 

```
"repository": {
    "type": "git",
    "url": "https://github.com/ageddesi/vite-ts-package-starter.git"
  },
```

2. Update publishConfig so it is pointing to the github package repository

```
"publishConfig": {
    "registry": "https://npm.pkg.github.com"
  },
```

3. If you are part of an organization on github, make sure you have that organization alias in your package.json name eg.

```
"name": "@org-alias/ts-npm-package-boilerplate",
```

If you are also using our github workflow to publish the package, you will need to update the registry defintion with the scope. 

Replace.

```
with:
    node-version: 16
    registry-url: https://npm.pkg.github.com/
```

with

```
with:
    node-version: 16
    registry-url: https://npm.pkg.github.com/
    scope: '@org-alias/'
```


4. If you are using our workflow to build and deploy to github you will need to first create a secret key and attach it to your repo with the following name.

```
secrets.GITHUB_TOKEN
```