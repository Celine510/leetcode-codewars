https://www.codewars.com/kata/546f922b54af40e1e90001da/javascript

https://codepen.io/Celine-10/pen/MWMXVBx

JavaScript

```js
function alphabetPosition(text) {
  return (
    text
      .split(' ')
      .join('')
      .toLowerCase()
      .match(/[a-z]/g)
      ?.map((item) => item.charCodeAt() - 96)
      .join(' ') ?? ''
  );
}
```