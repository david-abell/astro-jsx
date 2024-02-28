# Astro JSX/EsLint test repo

## Initial Setup

- Install minimum dependencies
  - @typescript-eslint/parser
  - eslint
  - eslint-plugin-astro
  - typescript-eslint
- add tsconfig.eslint.json and recommended .eslintrc.json w/ `overrides: [{...parserOptions: {..."project": "./tsconfig.eslint.json"}}]`

## Possible resolutions tested

### Astro add react

- `npx astro add react` resolves error
- also works even when changes are reverted and editor restarted
  - it appears astro or typescript is crawling `node_modules` for jsx definitions as error reappears only after reverting changes, deleting node_modules, and rerunning `npm install`
