(_The following is basically a short version of [this article](https://codeburst.io/explaining-value-vs-reference-in-javascript-647a975e12a0)_)

Primitives are accessed directly. Primitives are:

- `String`
- `Number`
- `Boolean`
- `null`
- `undefined`

Other data types are passed by reference (and handled as Objects in JavaScript):

- `Array`
- `Function`
- `Object`

When a primitive is assigned to a variable, its value is _copied_. For example:

```JavaScript
var x = 10
var a = x
var x = 'abc'

console.log(x) // => 'abc'
console.log(a) // => 10
```

Changes made to `x` after assigning `x` to `a` are not reflected in `a`, because its value copied and the variables have no connection whatsoever to on another.

In contrast, Objects are references to an address. If an Object is assigned to a variable, that variable contains a _reference_ to the address of the Object. Therefore, changes made to the object are reflected in all variables referencing that address.

```JavaScript
function invalidatePerson(person) {
	person.valid = false
}

var jenkins = {
	age: 25,
	valid: true
}

var invalidPerson = invalidatePerson(jenkins)

console.log(jenkins.valid) // => false
console.log(invalidPerson.valid) // => false
```
