# Aha-moments-in-JS
Just some Aha! moments in learning Javascript.


* #### `Object` is a function, not an object.
Similarly, `Array` is function, too.


* #### When used with one argument, `Object.create()` behaves the same as:
```
function object(o) {
	function F() {}
	F.prototype = o
	return new F()
}
```


* #### There are two types of properties in javascript objects, one is `data property`, and the other is `accessor property`.
when defined through `Object.defineProperty`, both `data property` and `accessor property` have these keys as descriptor:
`configurable`, `enumerable`, `value`, `writable`,
but an `accessor property` has `get` and `set`


* #### ES6 has formalized the `__proto__` property.

