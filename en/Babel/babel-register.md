# Babel Register

## Install

```shell
yarn add -D babel-register
```

## Usage

```js
require('babel-register')
```

## What it does

It makes all subsequent files required by node with extensions `.es6`, `.es`, `.jsx` , `.js` to be transformed by Babel.

This way, a node app can be written using Babel syntax.

Ref: [Babel Register - Babel](https://babeljs.io/docs/usage/babel-register/)