# Interview Questions

- [Capitalize All Words In A Sentence](#capitalize-all-words-in-a-sentence)

As an example, let's take an object with basic property that we want to clone
```
    const obj = [{name: "Viktor"}];
```

## Capitalize All Words In A Sentence
```js
function capitalize(sentence) {
    return sentence ? 
        sentence.split(' ').map(word => word[0].toUpperCase() + word.slice(1).toLowerCase()).join(' ') : ""
}

const str = "This is my personal world";

const result = capitalize(str);
```

## Check if word is palindrome

```js
function isPalindrome(str) {
 return str ?
  str.toLowerCase().split('').reverse().join('') === str.toLowerCase() : false
}

const str = 'Noon';

console.log(isPalindrome(str)) // true
```
