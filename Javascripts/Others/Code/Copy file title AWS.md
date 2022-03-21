---
id: 1647842378280
title: Copy file title AWS
category: Javascripts/Others/Code/
---

Console tab
```js
let str = "";
document.querySelectorAll(".js-file-title > a").forEach(a => str = str+= (a.innerText + "\n"));
console.log(str);
```
