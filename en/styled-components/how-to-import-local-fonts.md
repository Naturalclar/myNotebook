# How to import local fonts using styled-components

In order to import local fonts to apply to your webpage using styled-components,
you will need to import the font-files separately then apply it to global.

```js
import { injectGlobal } from 'styled-components';
import MyFont from './MyFont.otf';

injectGlobal`
  @font-face {
    font-family: MyFont;
    src: url('${MyFont}') format('opentype');
  }
`
```

You will need `file-loader` in order to import the font files.

`yarn add -D file-loader`

In your `webpack.config.js`, add test to load font files

```js
{
test: /\.(eot|svg|ttf|woff|woff2|otf)$/,
loader: 'file-loader',
}
```


## Reference
[Better explanation for font-face](https://github.com/styled-components/styled-components/issues/233)