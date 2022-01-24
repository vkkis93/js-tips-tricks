# Array

- [Clone an array](#clone-an-array)
As an example, let's take an object with basic property that we want to clone
```
    const obj = [{name: "Viktor"}];
```

# Clone an object
1. ES6 Spread Operator
```js
const newObj = {...obj};
```
6. Object.assign() 
```js
const newArr = Object.assign({}, obj);
```
7. JSON.parse && JSON.stringify [Deep copy]

```js
const newObj = JSON.parse(JSON.stringify(obj));
```
It is important to note that this method is not compatible with functions or dates, because JSON is not compatible with functions, and dates are converted to string by JSON.stringify.
For example
```js
const obj = {
  date: new Date(),
  search: new RegExp(/g/),
  getInfoV1: function() {console.log('v1')},
  getInfoV2: () => {console.log('v2')},
  isTest: true
}
const newObj = JSON.parse(JSON.stringify(obj));
//newObj
{ date: '2022-01-24T12:45:05.511Z', search: {}, isTest: true }
```
8. structuredClone() [Deep copy]

Warning! structuredClone() is not part of ECMAScript, it was added to the platform-specific parts of many platforms and is still widely available (either now or soon):
* Chrome 98
* Safari 137 (Technology Preview Release)
* Firefox 94
* Node.js 17.0
* Deno 1.14
```js
const newObj = structuredClone(obj);

```
