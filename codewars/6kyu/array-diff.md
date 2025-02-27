https://www.codewars.com/kata/523f5d21c841566fde000009/javascript

JavaScript

```js
function arrayDiff(a, b) {
  return a.filter(num => !b.includes(num));
}
```

```js
function arrayDiff(a, b) {
  return a.filter(x => b.indexOf(x) == -1 );
}
```

```js
function arrayDiff(a, b) {
  b.forEach(item => {
    a = a.filter(i => i != item)
  }) 
  return a
}
```
