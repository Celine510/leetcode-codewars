https://www.codewars.com/kata/5acfab8d23c81836c90000eb/javascript

https://codepen.io/Celine-10/pen/LEPwRbw

JavaScript

Math.ceil() :無條件進位
eval() :執行字串中的 JavaScript 表達式

```js
//2
function convertRecipe(recipe) {
  const ans = recipe.split(' ').map((item, index, arr) => {
    const op = (num) =>
      `${arr[index]} (${Math.ceil(num * eval(arr[index - 1]))}g)`;

    return item === 'tbsp' ? op(15) : item === 'tsp' ? op(5) : item;
  });
  return ans.join(' ');
}
```

```js
// 1
function convertRecipe(recipe) {
  const arr = recipe.split(' ');
  const ans = arr.map((item, index) => {
    const op = (num) => {
      const hasDiv = arr[index - 1].split('/');
      let g = 0;
      if (hasDiv.length > 1) {
        g = Math.ceil((num * hasDiv[0]) / (1 * hasDiv[1]));
      } else {
        g = num * arr[index - 1];
      }
      return `${arr[index]} (${g}g)`;
    };

    if (item === 'tbsp') return op(15);
    else if (item === 'tsp') return op(5);
    else return item;
  });
  return ans.join(' ')
}
```
