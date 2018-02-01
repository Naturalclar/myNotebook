# Rendering Lists by Iterating through a Loop

When creating a list in a react component, you can hard code each item in the list like in the following code:

```js
export default class HelloLists extends React.Component{
  render() {
    return(
      <ul>
        <li>This</li>
        <li>is</li>
        <li>a</li>
        <li>list</li>
      </ul>
    )
  }
}
```

However, hard coding the list items everytime can be a big pain, especially the number of items in the list is large.

Instead, you can use plain Javascript in the component and map each list items in an array.

```js
export default class HelloList extends React.Component{
  render() {
    const items = ['This', 'is', 'a', 'list'];
    return(
      <ul>
        {items.map((item) => {
	  return (
	    <li>{item}</li>
	  )
	}
      </ul>
    )
  }
}
```

This makes it much rendering of the list much simpler.

You could also set the output of the iteration inside a new variable, which makes the final return statement much shorter:

```js
export default class HelloList extends React.Component{
  render(){
    const items = ['This', 'is', 'a', 'list'];
    const listItems = items.map((item) => {
        return (
	  <li>{item}</li>
	)
      }
    return (
      <ul>{ listItems }</ul>
    )
  }
}
```