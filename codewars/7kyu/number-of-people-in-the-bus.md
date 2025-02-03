https://www.codewars.com/kata/5648b12ce68d9daa6b000099/javascript

https://codepen.io/Celine-10/pen/BagozVw

JavaScript

```js
// 3
var number = function(busStops) {
  return busStops.reduce((sum, item) => {
    return sum + item[0] - item[1]
  }, 0)
}
```

```js
// 2
var number = function(busStops) {
  return busStops.flat().reduce((sum, item, index) => sum += index % 2 ? -item : item, 0)
}
```

```js
// 1
var number = function (busStops) {
  let ans = 0;
  busStops.map((i) =>
    i.map((e, index) => { ans += index ? -e : e; })
  );
  return ans;
};
```
