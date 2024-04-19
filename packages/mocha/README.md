# `@egiftcard/eslint-config-mocha`

eGiftCard's [Mocha](https://mochajs.org/) ESLint configuration.

## Usage

```bash
yarn add --dev \
    @egiftcard/eslint-config@^12.0.0 \
    @egiftcard/eslint-config-mocha@^12.0.0 \
    eslint@^8.45.0 \
    eslint-config-prettier@^8.5.0 \
    eslint-plugin-import@~2.26.0 \
    eslint-plugin-jsdoc@^41.1.2 \
    eslint-plugin-mocha@^10.1.0 \
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
  root: true,

  extends: [
    // These should be added last unless you know what you're doing.
    '@egiftcard/eslint-config',
    '@egiftcard/eslint-config-mocha',
  ],
};
```

If your project has `prefer-arrow-callback` you will need to disable that and replace it with `mocha/prefer-arrow-callback`.
