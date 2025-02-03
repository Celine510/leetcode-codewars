https://www.codewars.com/kata/5498505a43e0fd83620010a9/javascript

https://codepen.io/Celine-10/pen/bGPvqPB

JavaScript

```js
function vectorAffinity(xs, ys) {
  let count = 0;
  for (let i = 0; i < xs.length; i++) {
    if (xs[i] === ys[i]) count++;
  }
  return !xs.length && !ys.length
    ? 1
    : count / (xs.length >= ys.length ? xs.length : ys.length);
}
```

```js
// Initial idea
function vectorAffinity(xs, ys) {
  if (xs.length === 0 && ys.length === 0) {
    return 1;
  }
  // aAry is an array with a relatively long length
  // bAry is another value
  const aAry = xs.lenght >= ys.length ? xs : ys;
  const bAry = aAry === xs ? ys : xs;

  return (
    bAry.reduce((total, item, i) => (total += item === aAry[i]), 0) /
    aAry.length
  );
}
```

```js
// 崴's solution
function vectorAffinity(xs, ys) {
  // JSON.stringify 遇到陣列內有 undefined 會出錯
  // JSON.stringify([undefined]) 會解析出 [null]
  if (JSON.stringify(xs) === JSON.stringify(ys)) return 1;

  let x = 0;
  let y = Math.max(xs.length, ys.length);
  // 從陣列的第一位開始刪，所以當其中一個被刪完就會跳出 while
  while (xs.length !== 0 && ys.length !== 0) {
    xs.splice(0, 1)[0] === ys.splice(0, 1)[0] ? (x += 1) : ':O';
  }
  return x / y;
}
```
