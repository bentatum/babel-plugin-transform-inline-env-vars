# babel-plugin-transform-inline-env-vars

Inline environment variables

## Example

### In

```js
// assuming process.env.NODE_ENV is actually "development"
process.env.NODE_ENV;
```

### Out

```js
"development";
```

## Installation

```sh
npm install babel-plugin-transform-inline-env-vars
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
// without options
{
  "plugins": ["transform-inline-env-vars"]
}

// with options
{
  "plugins": [
    ["transform-inline-env-vars", {
      "include": [
        "NODE_ENV"
      ]
    }]
  ]
}
```

### Via CLI

```sh
babel --plugins transform-inline-env-vars script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["transform-inline-env-vars"]
});
```

## Options

+ `include` - array of environment variables to include
+ `exclude` - array of environment variables to exclude
