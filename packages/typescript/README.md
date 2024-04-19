# `@egiftcard/eslint-config-typescript`

EgiftCard's [TypeScript](https://www.typescriptlang.org) ESLint configuration.

## Usage

```bash
yarn add --dev \
    eslint@^7.23.0 \
    eslint-plugin-import@^2.22.0 \
    @typescript-eslint/eslint-plugin@^3.9.1 \
    @typescript-eslint/parser@^3.9.1 \
    @egiftcard/eslint-config@^5.0.0 \
    @egiftcard/eslint-config-typescript@^5.0.0
```

The order in which you extend ESLint rules matters.
The `@egiftcard/*` eslint configs should be added to the `extends` array _last_,
with `@egiftcard/eslint-config` first, and `@egiftcard/eslint-config-*` in any
order thereafter.

```js
module.exports = {
  root: true,

  extends: [
    // This should be added last unless you know what you're doing.
    '@egiftcard/eslint-config',
  ],

  overrides: [
    // The TypeScript config disables certain rules that you want to keep for
    // non-TypeScript files, so it should be added in an override.
    {
      files: ['*.ts'],
      extends: [
        '@egiftcard/eslint-config-typescript',
      ],
    },
  ],
};
```
