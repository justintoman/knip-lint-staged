# Hello!

This is a repo to test that knip will report `lint-staged` as unused when it is used in a pre-commit hook by husky.

I've locked the versions for knip, lint-staged, and husky to ensure that the issue can be reproduced reliably.

## Usage

```bash
npm install
npm run knip
```

That should report:

```
Unused devDependencies (1)
lint-staged  package.json
```

Which should be incorrect because `lint-staged` is used in `.husky/pre-commit`.
