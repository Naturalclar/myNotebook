# Redux

## What is redux?

Redux is a state container for Javascript Web Apps.

Instead of each component holding its own state, we can use one state container for the whole app, so that it will behave consistently throughout the app.

State of whole app will be represented in a single Javascript object

Often use with React.

## How does it work?

Redux has three basic components, `actions`, `reducers`, and `store`

### Store

`store` is a container that holds state of the entire application.
This store will be passed down to the whole application so any components inside the application can get the application's state from it.

### Reducers

`reducer` is a set of function that waits for an `action`, then change the application's state according to the received `action`.

### Actions

`action` is a set of functions that can be `dispatched` by components, that will trigger `reducers` to change the state of application.

## How to set up redux

First, install dependencies 

`yarn add redux react-redux redux-thunk`

`react-redux` is a library that will bind `react` with `redux` as the name states.

`redux-thunk` is a middleware for `redux` that allows handling nested dispatch for performing asynchronous changes.



Ref: [Redux](http://redux.js.org/)