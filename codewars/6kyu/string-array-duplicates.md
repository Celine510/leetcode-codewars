https://www.codewars.com/kata/59f08f89a5e129c543000069/train/javascript

https://codepen.io/Celine-10/pen/JoPejry?editors=0010

JavaScript

```js
// 2
function dup2(s) {
  return s.map((item) =>
    item
      .split('')
      .filter((ele, i, arr) => ele !== arr[i - 1])
      .join('')
  );
}
```

```js
// 1
function dup(s) {
  const ans = s.map((item) => {
    const arr = [];
    item.split('').forEach((ele) => {
      if (ele !== arr.at(-1)) arr.push(ele);
    });
    return arr.join('');
  });
  return ans;
}
```
