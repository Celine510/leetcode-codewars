https://www.codewars.com/kata/57f6051c3ff02f3b7300008b/javascript

https://codepen.io/Celine-10/pen/mybZJex

JavaScript

```js
// 2
function meeting(x, need) {
  if (!need) return 'Game On';
  
  const ans = [];
  
  for (const [occupants, chairs] of x) {
    const available = chairs - occupants.length;
    if (available > 0) {
      const taken = Math.min(available, need);
      ans.push(taken);
      need -= taken;
    } else {
      ans.push(0);
    }

    if (need === 0) return ans;
  }

  return 'Not enough!';
}
```

```js
// 1
function meeting(x, need) {
  if (!need) return 'Game On';

  const ans = [];

  x.forEach((item) => {
    const num = item[1] - item[0].length;
    if (num > 0 && need !== 0) {
      if (num <= need) {
        ans.push(num);
        need -= num;
      } else if (num > need) {
        ans.push(need);
        need = 0;
      }
    } else if (need) ans.push(0);
  });
  return need > 0 ? 'Not enough!' : ans;
}
```
