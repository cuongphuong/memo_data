---
id: 1640583047823
title: Sort key by value in object
category: Javascripts/Others/Code/
---

```
var list = {"you": 100, "me": 75, "foo": 116, "bar": 15};
keysSorted = Object.keys(list).sort(function(a,b){return list[a]-list[b]})
console.log(keysSorted);     // bar,me,you,foo
```
---

[https://stackoverflow.com/questions/1069666/sorting-object-property-by-values](https://stackoverflow.com/questions/1069666/sorting-object-property-by-values)