# Introduction

Add style-resources-loader to your project easier.

# Installation

```
vue add style-resources-loader
```

# Config

Define your resource's patterns under `pluginOptions` in vue.config.js.

Example

```js
const path = require('path')
module.exports = {
  pluginOptions: {
    'style-resources-loader': {
      'patterns': [
        path.resolve(__dirname, 'src/styles/abstracts/*.styl'),
      ]
    }
  }
}
```
