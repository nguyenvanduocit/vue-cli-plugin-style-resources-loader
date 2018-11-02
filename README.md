# Introduction
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader?ref=badge_shield)


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
        path.resolve(__dirname, './src/styles/abstracts/*.styl'),
      ]
    }
  }
}
```


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader?ref=badge_large)
