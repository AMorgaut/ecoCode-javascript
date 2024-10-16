![Logo](https://github.com/green-code-initiative/ecoCode/blob/main/docs/resources/logo-large.png?raw=true)
======================================

An ESLint plugin which provides JavaScript and TypeScript rules of the ecoCode project.

👉 See [ecoCode-javascript README](../README.md) to have more information.

> ⚠️ This plugin is in a very early stage and need improvements. Any contribution will be appreciated.

🚀 Getting started
------------------

### Installation

You'll need to install [ESLint](https://eslint.org/) (v7 or newer) and this plugin:

```sh
# yarn
yarn add -D eslint @ecocode/eslint-plugin
# npm
npm install -D eslint @ecocode/eslint-plugin
```

> You are using TypeScript? You will also need to install [typescript-eslint](https://typescript-eslint.io/) to enable
> our rules.\
> Follow [this official guide](https://typescript-eslint.io/getting-started) to install it in a few steps.

#### Are you working with a GitHub Packages registry?

The plugin is also available from GitHub npm registry under "green-code-initiative" scope:

```sh
# yarn
yarn add -D eslint @green-code-initiative/ecocode-eslint-plugin
# npm
npm install -D eslint @green-code-initiative/ecocode-eslint-plugin
```

### Enable plugin with recommended configuration

#### With modern `eslint.config.js`

Add `@ecocode` **"flat/recommended"** configuration to  your `eslint.config.js`:

```js
import ecocode from '@ecocode/eslint-plugin'

export default [
  /* other eslint configurations */
  ecocode.configs['flat/recommended'],
]
```

#### With the legacy `.eslintrc` 

Add `@ecocode` **"recommended"** configuration to `extends` section of your `.eslintrc`:

```json
{
  "extends": ["plugin:@ecocode/recommended"]
}
```

### Enable specific rules

#### With modern `eslint.config.js`

Add the `ecocode` plugin configuration to your `eslint.config.js` and select the rules to activate:

```js
import ecocode from '@ecocode/eslint-plugin'

export default [
  /* other eslint configurations */
  {
    plugins: { "@ecocode": ecocode },
    rules: {
      "@ecocode/no-multiple-access-dom-element": "error"
    }
  }
]
```

#### With the legacy `.eslintrc` 

Add `@ecocode` to the `plugins` section of your `.eslintrc`, followed by rules configuration:

```jsonc
{
  "plugins": ["@ecocode"],
  "rules": {
    "@ecocode/no-multiple-access-dom-element": "error"
  }
}
```

🔨 Rules
--------

<!-- begin auto-generated rules list -->

⚠️ Configurations set to warn in.\
✅ Set in the `recommended` configuration.

| Name                                                                                   | Description                                                | ⚠️                            |
| :------------------------------------------------------------------------------------- | :--------------------------------------------------------- | :---------------------------- |
| [avoid-brightness-override](docs/rules/avoid-brightness-override.md)                   | Should avoid to override brightness                        | ✅ ![badge-flat/recommended][] |
| [avoid-css-animations](docs/rules/avoid-css-animations.md)                             | Avoid usage of CSS animations                              | ✅ ![badge-flat/recommended][] |
| [avoid-high-accuracy-geolocation](docs/rules/avoid-high-accuracy-geolocation.md)       | Avoid using high accuracy geolocation in web applications. | ✅ ![badge-flat/recommended][] |
| [limit-db-query-results](docs/rules/limit-db-query-results.md)                         | Should limit the number of returns for a SQL query         | ✅ ![badge-flat/recommended][] |
| [no-empty-image-src-attribute](docs/rules/no-empty-image-src-attribute.md)             | Disallow usage of image with empty source attribute        | ✅ ![badge-flat/recommended][] |
| [no-import-all-from-library](docs/rules/no-import-all-from-library.md)                 | Should not import all from library                         | ✅ ![badge-flat/recommended][] |
| [no-multiple-access-dom-element](docs/rules/no-multiple-access-dom-element.md)         | Disallow multiple access of same DOM element.              | ✅ ![badge-flat/recommended][] |
| [no-multiple-style-changes](docs/rules/no-multiple-style-changes.md)                   | Disallow multiple style changes at once.                   | ✅ ![badge-flat/recommended][] |
| [no-torch](docs/rules/no-torch.md)                                                     | Should not programmatically enable torch mode              | ✅ ![badge-flat/recommended][] |
| [prefer-collections-with-pagination](docs/rules/prefer-collections-with-pagination.md) | Prefer API collections with pagination.                    | ✅ ![badge-flat/recommended][] |
| [prefer-shorthand-css-notations](docs/rules/prefer-shorthand-css-notations.md)         | Encourage usage of shorthand CSS notations                 | ✅ ![badge-flat/recommended][] |
| [provide-print-css](docs/rules/provide-print-css.md)                                   | Enforce providing a print stylesheet                       | ✅ ![badge-flat/recommended][] |

<!-- end auto-generated rules list -->


🛒 Distribution
---------------

You can follow changelog on [GitHub Releases page](https://github.com/green-code-initiative/ecoCode-linter/releases).
