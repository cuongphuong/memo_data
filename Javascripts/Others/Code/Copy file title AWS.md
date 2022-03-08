---
id: 1646726725524
title: Copy file title AWS
category: Javascripts/Others/Code/
---

Console tab
```
let str = "";
document.querySelectorAll(".js-file-title > a").forEach(a => str = str+= (a.innerText + "\n"));
console.log(str);
```
