https://www.codewars.com/kata/58f8a3a27a5c28d92e000144/javascript

https://codepen.io/Celine-10/pen/GRbxWVJ

JavaScript

```js
function firstNonConsecutive(arr) {
  for (let i = 0; i < arr.length - 1; ++i) {
    if (arr[i] + 1 !== arr[i + 1]) {
      return arr[i + 1];
    }
  }
  return null;
}
```
