Given the array

```js
const arr = [0, 0, 0, 1, 2, 3, 3, 3, 4]
```

using `Set` we can create an array with only unique values in it

```js
const uniqueArr = [...new Set(arr)] // [0, 1, 2, 3, 4]
```
