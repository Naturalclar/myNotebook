# Separating Express Routing into separate files

When using express.js, you will have many routers that will each perform a specific app for the application.

As the application grows, the number of routers will increase, and you may also want to have a nested router for separate pages. If you have all that routers in a single file, the code will be a nightmare to maintain.

`express.js` provides a `Router` class to create a modular mountable rotue handlers.

## express.Router

We can create a router file named `birds.js` with the following content:

```
const express = require('express');
const router = express.Router();

// middleware that is specific to this router
router.use(function timeLog (req, res, next) {
    console.log('Time: ', Date.now());
    next();
});
// define the home page route
router.get('/', (req, res) => {
    res.send('Birds home page')
});
// define the about route
router.get('/about', (req, res) => {
    res.send('About birds');
});

module.exports = router

```

Then, you can load the router in `app.js`

```
const birds = require('./birds');

// ...

app.use('/birds', bitrds);

//...
```

The app will now be able to handle requests to `/birds` and `/birds/about,` as well as call the `timeLog` middleware function that is specific to this route.

Reference: 

[Express Routing Example](http://expressjs.com/en/guide/routing.html)