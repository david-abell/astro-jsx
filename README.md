# Astro JSX/EsLint test repo

## Initial Setup

- Install minimum dependencies
  - @typescript-eslint/parser
  - eslint
  - eslint-plugin-astro
  - typescript-eslint
- add tsconfig.eslint.json and recommended .eslintrc.json w/ `overrides: [{...parserOptions: {..."project": "./tsconfig.eslint.json"}}]`

## Possible resolutions tested

#### vs-code caching problems

Resolutions seem to also work even when changes are reverted and editor restarted as error reappears only after reverting changes. Error only returns after deleting node_modules and rerunning `npm install`

### Astro add jsx frameworks

- `npx astro add react` resolves error
- `npx astro add preact` resolves error
- `npx astro add solid-js` resolves error
- `npx astro add vue` does NOT resolve error

### Add JSX declaration file

ota-meshi's recommendation to add a jsx declaration file in project root such as `jsx.d.ts` resolves error

```ts
import "astro/astro-jsx";

declare global {
  namespace JSX {
    type Element = HTMLElement;
    // type Element = astroHTML.JSX.Element // We want to use this, but it is defined as any.
    type IntrinsicElements = astroHTML.JSX.IntrinsicElements;
  }
}
```
