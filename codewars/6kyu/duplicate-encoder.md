https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/javascript

https://codepen.io/Celine-10/pen/BaEYyyW

JavaScript

```js
// 2
function duplicateEncode(word) {
  return [...word.toLowerCase()]
    .map((item, index, ary) =>
      ary.lastIndexOf(item) === ary.indexOf(item) ? '(' : ')'
    )
    .join('');
}
```

```js
// 1
function duplicateEncode(word) {
  let ary = [...word.toLowerCase()];
  let newStr = '';
  for (let i = 0; i < ary.length; i++) {
    ary.lastIndexOf(ary[i]) === ary.indexOf(ary[i])
      ? (newStr += '(')
      : (newStr += ')');
  }
  return newStr;
}
```
