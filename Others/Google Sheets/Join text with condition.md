---
id: 1642131162552
title: Join text with condition
category: Others/Google Sheets/
---


`Input:`
```
=ARRAYFORMULA(TEXTJOIN(", ",TRUE,(IF(B1:B4="Red",C1:C4,""))))
```
`Output:`

```
1, 3
```


| A | B| C|
| --- | --- | --- |
| 1| TRUE| 1|
| 2| FALSE| 2|
| 3| TRUE| 3|
| 4| FALSE| 4|

---
`Source`: [https://www.automateexcel.com/formulas/textjoin-if/](https://www.automateexcel.com/formulas/textjoin-if/)

Tag: `Join text if`, `join if`