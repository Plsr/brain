#seed 

See: https://web.archive.org/web/20241211170720/https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976#.8h1rzm6vi


A pure function in JavaScript is a function with no side effects, every time you call it with the same arguments it returns the exact same result. Common disqualifies for a pure function are Methods like `Math.random()` and `Date.now()` being called. I the function has to manipulate an object, it has to manipulate a copy of it to not manipulate the external state.