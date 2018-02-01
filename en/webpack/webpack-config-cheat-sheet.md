# Webpack Config Cheat Sheet

## General

### Dependencies

`yarn add -D webpack`

```js

const webpack = require('webpack');

module.exports = {
  entry: `${__dirname}/src/main.js`,
  output: {
    path: `${__dirname}/public`,
    filename: 'bundle.js',
  },
  resolve: {
    extensions: ['.js','.jsx'] //jsx only if you'll be using react
  },
}

```

## Riot.js

### Dependencies

`yarn add -D babel-loader babel-preset-es2015-riot riot-tag-loader`
`yarn add riot`

```js

module.exports = {
  ...
  module: {
    loaders: [
      {
        test: /\.tag$/,
        enforce: 'pre',
        exclude: /node_modules/,
        use: [
          {
            loader: 'riot-tag-loader',
            query: {
              type: 'es6',
            }
          }
        ]
      },
      {
        test: /\.(tag|js)$/,
        exclude: /node_modules/,
        lodaer: 'babel-loader',
        options: {
          presets: ['es2015-riot'],
        }
      }
    ]
  },
  plugins: [
    new webpack.ProvidePlugin({
      riot: 'riot',
    }),
  ]
  ...
}

```


## jQuery 

### Dependencies

`yarn add jquery`

```js

module.exports = {
  ...
  plugins: [
    new webpack.ProvidePlugin({
      $: 'jquery',
      jQuery: 'jquery',
      'window.jQuery': 'jquery',
    })
  ]
  ...
}

```
