# JavaScript ES6 Style Configuration 

ES6 Style Configuration for [ESLint](http://eslint.org/).

## Usage 

```bash
$ npm install eslint-config-civa86 --save-dev
```

ESLint configuration

```json
{
    "extends": "civa86"
}
```

#### Webpack 1.x with eslint-loader

eslint-loader will search configuration in

- `.eslintrc` file at the root of the project
- `eslintConfig` property inside package.json

Example: package.json

```json
{
    "eslintConfig": {
        "extends": "civa86"
    }
}
```

#### Webpack 2.x with eslint-loader

In your webpack configuration

```javascript
module.exports = {
  // ...
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        loader: "eslint-loader",
        options: {
          extends: "civa86"
        }
      },
    ],
  },
  // ...
}
```
