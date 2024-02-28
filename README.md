# Astro JSX/EsLint test repo

## Steps taken

### Initial Setup

- Install minimum dependencies
  - @typescript-eslint/parser
  - eslint
  - eslint-plugin-astro
  - typescript-eslint
- add tsconfig.eslint.json and recommended .eslintrc.json w/ `overrides: [{...parserOptions: {..."project": "./tsconfig.eslint.json"}}]`
