---
id: 1646815811048
title: Sort by date
category: Javascripts/Others/Code/
---


# Simplest 


```
array.sort(function(a,b){
  // Turn your strings into dates, and then subtract them
  // to get a value that is either negative, positive, or zero.
  return new Date(b.date) - new Date(a.date);
});
```
Source: [https://stackoverflow.com/questions/10123953/how-to-sort-an-object-array-by-date-property]()