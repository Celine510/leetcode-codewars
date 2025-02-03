https://www.codewars.com/kata/5626b561280a42ecc50000d1/javascript

https://codepen.io/Celine-10/pen/oNrbYEy

JavaScript

```js
// 2
function sumDigPow(a, b) {
  const allNumAry = Array.from({ length: b - a + 1 }, (num, i) => a + i);

  const ans = allNumAry.filter((ele, index, array) => {
    let count = 0;
    ele
      .toString()
      .split('')
      .forEach((item, index) => {
        count += Math.pow(item, index + 1);
      });
    return ele === count;
  });
  return ans;
}
```

```js
// 1
function sumDigPow(a, b) {
  let ans = [];
  for (let i = a; i <= b; i++) {
    const n = i
      .toString()
      .split('')
      .reduce((sum, ele, index) => {
        return sum + Math.pow(ele, index + 1);
      }, 0);
    if (n === i) ans.push(n);
  }
  return ans;
}
```
