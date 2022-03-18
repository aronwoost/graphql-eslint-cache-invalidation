# eslint cache does not get invalidated when .graphqlconfig gets changed

### How to reproduce

- run `npm i`
- run `npm run lint` (✅)
- delete line `"schema": "./schema.graphql"` from `.graphqlconfig`
- run `npm run lint`

Result: linter is still passing.

Delete `.eslintcache` and run `npm run lint` again. Now it fails correctly.
