https://www.codewars.com/kata/514a024011ea4fb54200004b/javascript

https://codepen.io/Celine-10/pen/PorRyKb

JavaScript

```js
function domainName(url) {
  if (url.match('www')) {
    return url.split('www.')[1].split('.')[0];
  } else if (url.match('//')) {
    return url.split('//')[1].split('.')[0];
  } else {
    return url.split('.')[0];
  }
}
```
