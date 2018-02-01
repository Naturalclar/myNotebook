## Updating an Item in a Immutable List

When we want to change an item inside a List of Maps.

Following code will change the `count` parameter of a map that contains `third` as its `name` parameter to `4`.



```js
import { fromJS } from 'immutable';

// create an Immutable List of Maps
const list = fromJS([
  {name:'first', count: 0},
  {name:'second', count: 4},
  {name:'third', count: 3},
  {name:'fourth', count: 2},
]);

// Change the 'count' of 'third' element to 4
const updatedList = list.update(
  list.findIndex(item => item.get('name') === 'third'), 
  item => item.set('count', 4);
  }
); 
```

## Reference 

[Stack Overflow- How to update element inside list with immutablejs](https://stackoverflow.com/questions/29589753/how-to-update-element-inside-list-with-immutablejs)
