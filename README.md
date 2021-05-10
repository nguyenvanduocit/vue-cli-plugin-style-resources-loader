# Introduction
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader?ref=badge_shield)
[![npm version](https://badge.fury.io/js/vue-cli-plugin-style-resources-loader.svg)](https://badge.fury.io/js/vue-cli-plugin-style-resources-loader)


Add style-resources-loader to your project easier.

# Installation

```
vue add style-resources-loader
```

# Config

Define your resource's patterns under `pluginOptions` > `style-resources-loader` in file `vue.config.js`.

| Name         | Data type | Description                            |
|--------------|-----------|----------------------------------------|
| preProcessor | {string}  | One of: sass, scss, stylus, less       |
| patterns     | {string | string[]} | Path to the resources you would like to inject |
| injector     | {Function | 'prepend' | 'append'} | Controls the resources injection precisely |

## patterns

Please read more at [patterns](https://github.com/yenshih/style-resources-loader#patterns).

### Example

```js
const path = require('path')
module.exports = {
  pluginOptions: {
    'style-resources-loader': {
      'preProcessor': 'stylus',
      'patterns': [
        path.resolve(__dirname, './src/styles/abstracts/*.styl'),
      ],
      'injector': 'append'
    }
  }
}
```

```js

const path = require('path')
module.exports = {
  pluginOptions: {
    'style-resources-loader': {
      'preProcessor': 'stylus',
      'patterns': [
        path.resolve(__dirname, 'path/to/stylus/variables/*.styl'),
        path.resolve(__dirname, 'path/to/stylus/mixins/*.styl')
      ],
      'injector': (source, resources) => {
        const combineAll = type => resources
            .filter(({ file }) => file.includes(type))
            .map(({ content }) => content)
            .join('');

        return combineAll('variables') + combineAll('mixins') + source;
    }
    }
  }
}
```
## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnguyenvanduocit%2Fvue-cli-plugin-style-resources-loader?ref=badge_large)
