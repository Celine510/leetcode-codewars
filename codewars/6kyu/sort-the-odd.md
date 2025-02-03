https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/javascript

https://codepen.io/Celine-10/pen/VYZEdwv

JavaScript

```js
function sortArray(array) {
  const oddList = array.filter((item) => item % 2 !== 0).sort((a, b) => a - b);

  const ans = array.map((item) => (item % 2 !== 0 ? oddList.shift() : item));

  return ans;
}
```

```js
// A simpler version in the answer
function sortArray(array) {
  const odd = array.filter((x) => x % 2).sort((a, b) => a - b);
  return array.map((x) => (x % 2 ? odd.shift() : x));
}
```
