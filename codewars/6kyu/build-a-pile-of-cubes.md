https://www.codewars.com/kata/5592e3bd57b64d00f3000047/javascript

https://codepen.io/Celine-10/pen/BagVPPY

JavaScript

```js
function findNb(m) {
  let sum = m;
  let n = 0;
  do {
    n += 1;
    sum = sum - n ** 3;
  } while (sum > 0);

  return sum >= 0 ? n : -1;
}
```
