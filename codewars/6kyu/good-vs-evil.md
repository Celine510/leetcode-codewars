https://www.codewars.com/kata/52761ee4cffbc69732000738/javascript

https://codepen.io/Celine-10/pen/mybYWBM

JavaScript

```js
function goodVsEvil(good, evil) {
  const gg = [1,2,3,3,4,10];
  const eg = [1,2,2,2,3,5,10];
  const gr = good.split(' ').reduce((sum, item, index) => sum += item * gg[index], 0);
  const er = evil.split(' ').reduce((sum, item, index) => sum += item * eg[index], 0);
  
  return gr === er
  ? "Battle Result: No victor on this battle field"
  : gr > er
  ? "Battle Result: Good triumphs over Evil"
  : "Battle Result: Evil eradicates all trace of Good"
}
```
