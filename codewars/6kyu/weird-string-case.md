https://www.codewars.com/kata/52b757663a95b11b3d00062d/javascript

https://codepen.io/Celine-10/pen/abgYMZO

JavaScript

```js
function toWeirdCase(string) {
  return string
    .toUpperCase()
    .split(' ')
    .map((item) =>
      item
        .split('')
        .map((ele, i) => (i % 2 ? ele.toLowerCase() : ele))
        .join('')
    )
    .join(' ');
}
```
