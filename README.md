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

### Booleans
A boolean is your good ol' true or false, and *any* type can be converted into a Boolean by doing a 'double-bang':
```js
let string = 'Hello there';
const isStr = !!string;
console.log(isStr);
// => true
```

### Numbers and Bigints
`Number`s are your regular numbers, like `45`, `13.3` and `42424242`. `Bigint`s, on the other hand, are denoted with an `n` after, like `34n`, `7438924290n` and `123n`. In a `bigint`, you can only use whole numbers (hence the `int` in the name) and you can have numbers larger than `Number.MAX_VALUE` by creating one via a string, e.g. `Biginit('1234567890123456789');` and you will get an accurate number. Using the literal syntax can only be so precise as you are using `Number`s.

### Strings
Strings are your 'text', and these are used in nearly every javascript application. There are hundreds of ways to use these, but here are two basic pointers for now.
* Empty strings (`''`) evaluate to false.
* Any value can be coerced to a string by doing `String(value);`

## Objects
There are many types of objects, so I will showcase how to test for which type of object, as well on the basics of it.
A value is considered an `object` if `typeof value === 'object'` evaluates to `true`.
The objects in this document are:
* `Array`
* `Set`
* `Object`
* `Map`
This will not cover `WeakMap`s and `WeakSet`s.

Objects declared with `const` are still mutable, such as `const out = {}`. You can still modify `out` by doing stuff like `out['prop'] = 'value';`.

### Array
Arrays are 0-based indexed objects.
When created via constructor function, you get 'empty' spaces
```js
const array = Array(5);
console.log(array);
// => [ <5 empty items> ]
```
You can overcome this by using the `fill` function.
```js
const array = Array(5).fill(0);
console.log(array);
// => [ 0, 0, 0, 0, 0 ]
```
This will fill *every* element with the value given.
#### Array methods
`Array.from` can create an array from any array-like value. This includes other Arrays and Sets.
