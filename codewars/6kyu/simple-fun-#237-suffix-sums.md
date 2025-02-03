https://www.codewars.com/kata/590938089ff3d186cb00004c/javascript

https://codepen.io/Celine-10/pen/vYqaaBB

JavaScript

```js
// 2
function suffixSums(a) {
  let na = [...a];
  let n = 0;
  return a.map((item, i, ar) => {
    if (n != 0) na.shift(n);
    n += 1;
    return na.reduce((sum, item) => (sum += item), 0);
  });
}
```

```js
// 1
function suffixSums(a) {
  let arr = [];
  let na = [...a];
  for (let i = 0; i < a.length; i++) {
    arr.push(na.reduce((sum, item) => (sum += item), 0));
    na.shift();
  }
  return arr;
}
```
