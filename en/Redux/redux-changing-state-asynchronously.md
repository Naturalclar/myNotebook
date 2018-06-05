# Async Redux

If the application needs to make communication beween client and server, there may be a need to communicate asynchronously using `fetch`.

In order to incorporate state change asynchronously, there will need to be 3 state of action for each api call.

- An action informing the reducers that the request has began

  The reducers can toggle an `isFetching` state to load a spinner for the client

- An action informing the reducers that the request has completed

  The reducers can toggle an `isFetching` state to turn off the spinner, and display the received result.

- An action informing the reducers that the request failed

  The reducers can toggle an `isFetching` state to turn off the spinner, and display an error message

## Reference
- [Async Actions - Redux](http://redux.js.org/docs/advanced/AsyncActions.html)