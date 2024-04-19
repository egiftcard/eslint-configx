# `@egiftcard/eslint-config-nodejs`

eGiftCard's [Node.js](https://nodejs.org) ESLint configuration.

## Usage

```bash
yarn add --dev \
    @egiftcard/eslint-config@^12.0.0 \
    @egiftcard/eslint-config-nodejs@^12.0.0 \
    eslint@^8.45.0 \
    eslint-config-prettier@^8.5.0 \
    eslint-plugin-import@~2.26.0 \
    eslint-plugin-jsdoc@^41.1.2 \
    eslint-plugin-n@^15.7.0 \
    eslint-plugin-prettier@^4.2.1 \
    eslint-plugin-promise@^6.1.1 \
    prettier@^2.7.1
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
};
```

To lint the `.eslintrc.js` file itself, you will **need** to add this config in addition to the base config.
