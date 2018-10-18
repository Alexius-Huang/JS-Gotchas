# Type Checking

## How to check if an object is a **JavaScript object** or an **Array**?

### Answer

`Array.isArray` is a good way to check whether an object is an Array.

```js
Array.isArray([1, 2, 3]);
// => true

Array.isArray({ a: 1, b: 2, c: 3 });
// => false
```

You can also use `instanceof Array` to check the object:

```js
[1, 2, 3] instanceof Array;
// => true

({ a: 1, b: 2, c: 3 }) instanceof Array;
// => false
```
