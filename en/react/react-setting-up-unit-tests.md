# How to set up unit test with React

`jest` is a testing library for JavaScript made by Facebook.
`enzyme` is a testing utility for React made by AirBnb, it works well with `jest`.

First, install dependencies.

`yarn add jest enzyme enzyme-adapter-react-16`

You will need a `.babelrc` file for your babel config if you don't have one already.

```json
{
  "presets": ["env", "react"]
}
```

In your `src` folder, create a setup file `setUpTests.js` with the following content.

```js
import Enzyme from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';

Enzyme.configure({ adapter: new Adapter() });
```

Also, create a `__mock__` folder in your `src` folder with the `fileMock.js` and `styleMock.js` with the following content:

```js
//fileMock.js
module.exports = 'test-file-stub';
```

```js
//styleMock.js
module.exports = {};
```

then, in your `package.json` file, add the following config:

```json
  "jest": {
    "setupTestFrameworkScriptFile": "<rootDir>/src/setUpTests.js",
    "moduleNameMapper": {
      "\\.(jpg|jpeg|png|gif|eot|otf|webp|svg|ttf|woff|woff2|mp4|webm|wav|mp3|m4a|aac|oga)$": "<rootDir>/src/__mocks__/fileMock.js",
      "\\.(css|less)$": "<rootDir>/src/__mocks__/styleMock.js"
    }
  }
```