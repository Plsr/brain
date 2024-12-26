There is no native `sum()` function on JavaScript arrays, so the sum has to be calculated by hand somehow.
There is the method `reduce()` on array, though.

> The reduce() method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

So, to sum the values of an array, we can simply use `reduce()` in a way like this (ES6 Syntax):

```JavaScript
const array = [1, 2, 3, 4]
const arraySum = array.reduce((sum, value) => sum + value, 1)
console.log(arraySum) // -> 10
```

[Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce?v=b)
