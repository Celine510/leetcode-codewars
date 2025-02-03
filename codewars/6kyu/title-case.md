https://www.codewars.com/kata/5202ef17a402dd033c000009/javascript

https://codepen.io/Celine-10/pen/eYwMvqr

JavaScript

```js
function titleCase(title, minorWords) {
  if (title.length === 0) return title;
  return title
    .toLowerCase()
    .split(' ')
    .map((item, index) => {
      if (
        minorWords &&
        minorWords
          .toLowerCase()
          .split(' ')
          .some((ele) => ele === item) &&
        index !== 0
      )
        return item;
      return item.at(0).toUpperCase() + item.substr(1);
    })
    .join(' ');
}
```
