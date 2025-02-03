https://www.codewars.com/kata/5410c0e6a0e736cf5b000e69/javascript

https://codepen.io/Celine-10/pen/abgYMWd

JavaScript

```js
// 2
function hamming(a, b) {
  return a.split('').filter((ele, i) => ele !== b[i]).length;
}
```

```js
// 1
function hamming(a, b) {
  return a
    .split('')
    .map((ele, i) => {
      if (ele !== b.split('')[i]) return ele;
    })
    .join('').length;
}
```
