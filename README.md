# rf-07

## Rendering Arrays in React

Whenever you render an array of React elements each element must be given a unique `key` prop.

Do not use the array index to assign the `key` prop since the `key` prop helps React keep track of elements between updates. Use a constant value. 

The `key` only needs to be unique within a given array. So this is fine:

```
const element = (
  <ul>
    {list.map(listItem => (
      <li key={listItem.id}>{listItem.value}</li>
    ))}
    {list.map(listItem => (
      <li key={listItem.id}>{listItem.value}</li>
    ))}
  </ul>
```
  
You can intentionally reset the state of a component by changing the `key`.
