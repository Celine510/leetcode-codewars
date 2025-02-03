https://www.codewars.com/kata/56786a687e9a88d1cf00005d/javascript

https://codepen.io/Celine-10/pen/jORaVVP

JavaScript

```js
// 2
function validateWord(s) {
  var freq = {};
  s.toLowerCase()
    .split('')
    .forEach(function (s) {
      freq[s] ? freq[s]++ : (freq[s] = 1);
    });

  return new Set(Object.values(freq)).size == 1;
}
```

```js
// 1
function validateWord(s) {
  let obj = {};
  [...s].forEach((item) => {
    if (!obj[item.toLowerCase()]) obj[item.toLowerCase()] = 0;
    obj[item.toLowerCase()]++;
  });
  const ary = Object.values(obj).sort((a, b) => a - b);
  return ary[0] === ary[ary.length - 1];
}
```
