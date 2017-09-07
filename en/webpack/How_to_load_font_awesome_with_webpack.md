# How to load font-awesome with webpack

In order to load font-awesome with webpack, you will need to load the css file as well as the font files.

First, install the font-awesome via npm.

`npm i -S font-awesome`

Then, install the following dependencies.

`npm i -D font-loader url-loader style-loader css-loader`

Then in `webpack.config.js`, add the following entry in the module.

```js
module: {
  ...
  {
    test:/\.css$/,
    use: [
      'style-loader',
      'css-loader',
    ],
  },
  {
    test: /\.woff2?(\?v=\d+\.\d+\.\d+)?$/,
    use: 'url-loader?limit=10000&mimeyupe=application/font-woff',
  },
  {
    test: /\.(ttf|eot|svg)(\?[\s\S]+)?$/,
    use: 'file-loader?name=./[name].[ext]',
  },
}
```

After that, you can import and use font-awesome in your project.

```js
import 'font-awesome/css/font-awesome.css';

...

```