https://www.codewars.com/kata/5541f58a944b85ce6d00006a/javascript

https://codepen.io/Celine-10/pen/yLdKMdP

JavaScript

```js
// 2
function productFib(n) {
  let a = 0;
  let b = 1;
  while (a * b <= n) {
    let c = a + b;
    a = b;
    b = c;
  }
  return [b - a, a, a * (b - a) === n];
}
```

```js
// 1
function productFib(n) {
  const arr = [0, 1];
  while (arr.at(-1) * arr.at(-2) !== n && arr.at(-1) * arr.at(-2) < n) {
    arr.push(arr.at(-1) + arr.at(-2));
  }
  return [arr.at(-2), arr.at(-1), arr.at(-1) * arr.at(-2) === n];
}
```
