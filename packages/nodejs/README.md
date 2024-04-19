# `@egiftcard/eslint-config-nodejs`

EgiftCard's [Node.js](https://nodejs.org) ESLint configuration.

## Usage

```bash
yarn add --dev \
    eslint@^7.23.0 \
    eslint-plugin-import@^2.22.0 \
    eslint-plugin-node@^11.1.0 \
    @egiftcard/eslint-config@^5.0.0 \
    @egiftcard/eslint-config-nodejs@^5.0.0
```

The order in which you extend ESLint rules matters.
The `@egiftcard/*` eslint configs should be added to the `extends` array _last_,
with `@egiftcard/eslint-config` first, and `@egiftcard/eslint-config-*` in any
order thereafter.

```js
module.exports = {
  extends: [
    // These should be added last unless you know what you're doing.
    '@egiftcard/eslint-config',
    '@egiftcard/eslint-config-nodejs',
  ],
}
```

To lint the `.eslintrc.js` file itself, you will **need** to add this config in addition to the base config.
