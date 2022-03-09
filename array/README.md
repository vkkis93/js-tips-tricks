# Array
- [Create an array containing 1-N elements](#Create-an-array-containig-1-n-elements)
- [Convert values in array](#convert-values-in-array)
- [Clone an array](#clone-an-array)
- [Find min and max value](#find-min-and-max-value)
- [Remove duplicates from arrays](#remove-duplicates-from-arrays)
- [Merge two arrays](#merge-two-arrays)
- [Recursively flattens array](#recursively-flattens-array)
- [Determines whether the passed value is an Array](#determines-whether-the-passed-value-is-an-array)
- [Get the difference between two arrays](#get-the-difference-between-two-arrays)
- [Sort array of numbers with native method sort](#sort-array-of-numbers-with-native-method-sort)

- [Creates an array of unique values that are included in arrays](#'creates-an-array-of-unique-values-that-are-included-in-arrays')
##Create an array containing 1-N elements
1. Array.from() + Array.keys()
```js
const arr = Array.from(Array(100).keys()) //[0, 1, 2, 3, .... 99]
```

2. Spread Operator
```js
const arr = [...Array(100).keys()]
```


##Convert values in array
```js
const arr = [1, "2", [[3]], false];
arr.map(Number) // [1, 2, 3, 0]
```

## Clone an array
As an example, let's take an array of numbers that we want to clone
```
     const arr = [1,2,3];
```
**1. ES6 Spread Operator**
```js
const newArr = [...arr];
```
**2. Slice()**

```js
const newArr = arr.slice();
```
**3. Array.from()**

```js
const newArr = Array.from(arr)
```
**4. Map()**
```js
const newArr = arr.map(x => x);
```
**5. Concat()**
```js
const newArr = [].concat(arr)
```
**6. Object.assign()** 
```js
const newArr = Object.assign([], arr);
```
**7. JSON.parse && JSON.stringify [Deep copy]**

```js
const newArr = JSON.parse(JSON.stringify(arr));
```

**8. structuredClone() [Deep copy]**

Warning! structuredClone() is not part of ECMAScript, it was added to the platform-specific parts of many platforms and is still widely available (either now or soon):
* Chrome 98
* Safari 137 (Technology Preview Release)
* Firefox 94
* Node.js 17.0
* Deno 1.14
```js
const newArr = structuredClone(myOriginal);

```
## Find min and max value
**By using reduce**
```js
const numbers = [2, 4, 16, 1024, 32, 64, 128, 256];
numbers.reduce((a, b) => a > b ? a : b); //max
numbers.reduce((a, b) => a < b ? a : b); //min
```
**By Math.min/max**
```js
const numbers = [2, 4, 16, 1024, 32, 64, 128, 256];
Math.max(...numbers); //max
Math.min(...numbers); //min
```
## Remove duplicates from arrays
```js
const numbers = [1, 5, 5, 5, 10, 10, 100, 1];
const uniqNumbers = [...new Set(numbers)]; ///[1, 5, 10, 100]

```

## Merge two arrays
1.Array.concat();
```js
const arr1 = [1,2,3];
const arr2 = ['a', 'b', 'c'];
const mergedArr = arr1.concat(arr2);
```

2. Spread Operator;
```js
const arr1 = [1,2,3];
const arr2 = ['a', 'b', 'c'];
const mergedArr = [...arr1, ...arr2];
```
3. Object.assign()
```js
const arr1 = [1,2,3];
const arr2 = ['a', 'b', 'c'];
const mergedArr = Object.assign(arr1, arr2);
```
## Recursively flattens array ES2019 (analog to lodash _.flattenDeep)
```js
const arr = [1, 'a', [2, ['b', ['c'], [['d']]], 3]];
arr.flat(Infinity) //[1, 'a', 2, 'b', 'c', 'd', 3]
```
## Determines whether the passed value is an Array
```js
console.log(Array.isArray([1, 2, 3])) // true
```
## Get the difference between two arrays
```js
const arr1 = [1, 2, 3];
const arr2 = [0, 2, 4];
const diff = arr1.filter(x => !arr2.includes(x));
```
## Creates an array of unique values that are included in arrays
```js
const arr1 = [1, 2, 3];
const arr2 = [0, 2, 4];
               
const difference = arr1
    .filter(x => !arr2.includes(x))
    .concat(arr2.filter(x => !arr1.includes(x))) //[1, 3, 0, 4]
```

## Sort array of numbers with native method sort
```js
const arr = new Float64Array[1, 2, 2, 2, 3, 1.5, 1.9, 10, 5, 19, 100, 30];
const sortedArr = [...arr.sort()] // [1, 1.5, 1.9, 2, 2, 2, 3, 5, 10, 19, 30, 100]

```
