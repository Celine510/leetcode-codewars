https://www.codewars.com/kata/577e277c9fb2a5511c00001d/javascript

https://codepen.io/Celine-10/pen/vEBqEgX

JavaScript

```js
function vowelShift(text, n) {
  if (!text || n === 0) return text;
  const rullArr = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U'];

  const vowels = text.split('').filter((item) => rullArr.includes(item));

  if (n > 0) {
    while (n--) vowels.unshift(vowels.pop());
  } else {
    while (n++) vowels.push(vowels.shift());
  }

  return text
    .split('')
    .map((item) => (rullArr.includes(item) ? vowels.shift(1) : item))
    .join('');
}
```
