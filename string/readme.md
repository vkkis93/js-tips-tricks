# String

- [Converts the first character of string](#converts-the-first-character-of-string)


# Converts the first character of string
```js

function capitalize(str) {
    return str ? str.charAt(0).toUpperCase() + str.substr(1).toLowerCase() : ""
}
const str = 'farting';

console.log(capitalize(str)) // Farting

```
