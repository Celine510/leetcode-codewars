https://www.codewars.com/kata/58f6000bc0ec6451960000fd

https://codepen.io/Celine-10/pen/mybzKQq

JavaScript

```js
function selReverse(arr, len) {
  if (!len) return arr;

  const num = arr.length / len;
  const ans = [];
  for (let i = 0; i < num; i++) {
    ans.push(arr.splice(0, len).reverse());
  }
  return ans.flat();
}
```
