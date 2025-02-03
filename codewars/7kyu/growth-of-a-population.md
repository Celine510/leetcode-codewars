https://www.codewars.com/kata/563b662a59afc2b5120000c6/javascript

https://codepen.io/Celine-10/pen/NWZWYjO

JavaScript

```js
// p0（初始人口）、percent（每年人口增長百分比）、aug（每年來的居民數）、p（目標人口數）
function nbYear(p0, percent, aug, p) {
  let count = 0;
  while (p0 < p) {
    p0 = Number.parseInt(p0 * (1 + percent * 0.01) + aug);
    count++;
  }
  return count;
}
```
