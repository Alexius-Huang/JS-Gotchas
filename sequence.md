# Sequence

## Initializing / Generating / Copying Array

### Answer

1. Using `Array.from`

```js
/* Copying an Array */
Array.from([1, 2, 3]);
// => [1, 2, 3]

/* Convert ES6 Map object / keys / values back into Array */
const m = new Map([['a', 1], ['b', 2], ['c', 3]]);

Array.from(m);
// => [['a', 1], ['b', 2], ['c', 3]]
Array.from(m.keys());
// => ['a', 'b', 'c']
Array.from(m.values());
// => [1, 2, 3]

/* Convert ES6 Set back into Array */
const s = new Set([1, 2, 3, 'a', 'b' , 'c']);

Array.from(s);
// => [1, 2, 3, 'a', 'b', 'c']
```

2. Using spread-rest operator `...`

```js
/* Copying an Array */
const arr = [1, 2, 3];

[...arr];
// => [1, 2, 3]

/* Convert ES6 Map object / keys / values back into Array */
const m = new Map([['a', 1], ['b', 2], ['c', 3]]);

[...m];
// => [['a', 1], ['b', 2], ['c', 3]]
[...m.keys()];
// => ['a', 'b', 'c']
[...m.values()];
// => [1, 2, 3]

/* Convert ES6 Set back into Array */
const s = new Set([1, 2, 3, 'a', 'b' , 'c']);

[...s];
// => [1, 2, 3, 'a', 'b', 'c']
```

3. **[TODO]** Custom array generating using `Symbol.Iterator`

## How to generate a sequence of number from 0 to (n - 1) ?

### Answer

1. Plain old `for` loop:

```js
const arr = [];
for (let i = 0; i < n; i++) {
  arr.push(i);
}
```

2. Using `Array.from` with `Array.prototype.map` method:

```js
const arr = Array.from(Array(n)).map((_, i) => i);
```
