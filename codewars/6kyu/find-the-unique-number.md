https://www.codewars.com/kata/585d7d5adb20cf33cb000235/train/javascript

JavaScript

```js
function findUniq(arr) {
  return arr.find(n => arr.indexOf(n) === arr.lastIndexOf(n));
}
```

```js
function findUniq(arr) {
  const na = new Set(arr);
  let res = 0;
  na.forEach((item) => {
    if (arr.indexOf(item) === arr.lastIndexOf(item)) res = item;
  });
  return res;
}
```
