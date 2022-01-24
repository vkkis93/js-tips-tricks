# Array

- [Clone an array](#clone-an-array)

As an example, let's take an array of numbers that we want to clone
```
     const arr = [1,2,3];
```

# Clone an array
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
