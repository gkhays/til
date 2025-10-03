# JavaScript Hoisting

> JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.

But not the initialization.

## Prefer Let Over Var

Confession: I typically peform declarations using `let` because it was strongly suggested, but I didn't know why. Now I do.

Whereas `let` is also hoisted but not initialized with a default variable.

The following outputs `undefined`.

```js
console.log(foo);
var foo = 'foo';
```

### References
1. [Let’s play… Does your code suck? JavaScript Variables Edition](https://youtube.com/shorts/ZRjmGq1gAEQ?si=RhZoRWBcp777dNaQ)
2. [MDN | Hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)
3. [What is Hoisting in JavaScript?](https://www.freecodecamp.org/news/what-is-hoisting-in-javascript/)