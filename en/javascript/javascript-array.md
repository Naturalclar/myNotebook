# Array.from()

From ES6, `Array.from()` method can be used to create an array from a range of numbers, much like python's `range()`

```js

//Creating an array from 0 to length-1
Array.from({length: 5}, (k, v) => v);
//[0, 1, 2, 3, 4]

//Creating an array from -5 to 5
Array.from({length:11}, (k, v) => v - 5);
//[-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5];

//Creating an array that doubles each number of given array
Array.from([1,2,3], x => x + x);
// [2, 4, 6]

```

## Reference
- [Array.from() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)