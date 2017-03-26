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


* #### The `executor` in `new Promise()` is executed immediately.
Say,
```
var p = new Promise(function(resolve, reject) {
	console.log('Yeah');
	resolve(42);
})
```
will log the `Yeah` right after this declaration.


* #### About `Object.freeze()` and `Object.seal()`
freeze:  prevents new properties from being added to it; prevents existing properties from being removed; and prevents existing properties, or their enumerability, configurability, or writability, from being changed.  The method returns the object being frozen.

seal: preventing new properties from being added to it and marking all existing properties as non-configurable. Values of present properties can still be changed as long as they are writable.


Notice that `freeze` is shallow, you have to do a `deepFreeze` to make it a real constant. And there is no error throwing out  when you trying to change the freezed object's property.


**keep updating**
