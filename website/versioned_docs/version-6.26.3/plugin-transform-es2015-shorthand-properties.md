---
id: version-6.26.3-babel-plugin-transform-es2015-shorthand-properties
title: babel-plugin-transform-es2015-shorthand-properties
sidebar_label: transform-es2015-shorthand-properties
original_id: babel-plugin-transform-es2015-shorthand-properties
---

## Example

**In**

```js
var o = { a, b, c };
```

**Out**

```js
var o = { a: a, b: b, c: c };
```

**In**

```js
var cat = {
  getName() {
    return name;
  }
};
```

**Out**

```js
var cat = {
  getName: function () {
    return name;
  }
};
```

## Installation

```sh
npm install --save-dev babel-plugin-transform-es2015-shorthand-properties
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  "plugins": ["transform-es2015-shorthand-properties"]
}
```

### Via CLI

```sh
babel --plugins transform-es2015-shorthand-properties script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["transform-es2015-shorthand-properties"]
});
```

