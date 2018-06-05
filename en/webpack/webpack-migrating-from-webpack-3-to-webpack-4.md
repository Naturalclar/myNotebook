# Migrating from Webpack 3 config to Webpack 4 config

List of steps I took to migrate from Webpack 3 to Webpack 4

## Adding Webpack-Cli

When you're migrating from webpack 3 to webpack 4,
you will need to add another dependency in your project, called `webpack-cli`.

`yarn add -D webpack webpack-cli`

## Changing Config slightly

Also, in your config file, change the `loaders` under `module` to `rules`

```js
//webpack.config.js - webpack 3
module.exports {
  ...
  modiule: {
    loaders: [
      {
        ...
      }
    ]
  }
  ...
}

```


```js
//webpack.config.js - webpack 4
module.exports {
  ...
  modiule: {
    rules: [
      {
        ...
      }
    ]
  }
  ...
}

```


## Reference
[Webpack doc](https://webpack.js.org/concepts/loaders)
