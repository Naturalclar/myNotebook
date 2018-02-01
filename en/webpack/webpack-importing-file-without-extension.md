# Importing Files without writing extension

When using `import` statement to import other module from different files, you usually need to write the file extension, such as below.

```
import '/modules/my-module.js';
import '/components/my-components.jsx';
```

In `webpack`, you can use the `resolve.extension` option, which will automatically resolve extensions specified in the array. 

Add the option below to your `webpack.config.js`.

```
module.exports = {
  ...
  resolve: {
    extensions: ['.js', '.jsx']
  },
  ...
```

After that, you can start importing files without writing the file extension every time.

```
import '/modules/my-module';
import '/components/mycomponents';
```