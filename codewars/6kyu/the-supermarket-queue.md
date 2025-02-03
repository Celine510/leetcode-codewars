https://www.codewars.com/kata/57b06f90e298a7b53d000a86/javascript

https://codepen.io/Celine-10/pen/BagrWXz

JavaScript

```js
function queueTime(customers, n) {
  let arr = [];
  customers.forEach((item) => {
    if (arr.length < n) {
      arr.push(item);
    } else {
      arr.sort((a, b) => a - b);
      arr[0] += item;
    }
  });
  // Get the maximum value of the array
  return Math.max.apply(null, arr) ?? 0;
}
```
