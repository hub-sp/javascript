# JavaScript Tutorial (Node.js)

|Table Of Contents|
:---:
|[Primitives](#Primitives)|
|[Objects](#Objects)|

## Syntax and Version
This info is based on Node.js v12.6.0 and using es6 syntax with up to es2020 features. You can always use a transpiler if necessary.

## Primitives

There are 6 primitives as of Node.js v12.6.0
* `null`
* `undefined`
* `string`
* `number`
* `bigint`
* `boolean`

### Null
`null`, essentially, is nothing. It is used when you want to convey that there is no data at that location.
Interestingly, `null` is an object!
```js
console.log(typeof null);
// => 'object'
```

### Undefined
`undefined` is the type you get when you initialize a variable with no value.
```js
let thing;
console.log(thing);
// => undefined
```
You usually do not assign this to anything directly, but is used primarily to check for the presence of something.

### Boolean
A boolean is your good ol' true or false, and *any* type can be converted into a Boolean by doing a 'double-bang':
```js
let string = 'Hello there';
const isStr = !!string;
console.log(isStr);
// => true
```
