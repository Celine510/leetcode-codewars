https://www.codewars.com/kata/5fc7d2d2682ff3000e1a3fbc/javascript

https://codepen.io/Celine-10/pen/jEOOrmg

JavaScript

```js
function isAValidMessage(msg) {
  const arr = msg.split(/(\d+)/);
  let ans = true;
  arr.forEach((item, index) => {
    if (item === '' || Number.isNaN(item * 1)) return;
    else if (item * 1 !== arr[index + 1].length) ans = false;
  });
  return ans;
}
```
