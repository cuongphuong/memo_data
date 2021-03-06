---
id: 1647846647098
title: Revealing Module Pattern
category: Javascripts/Design Pattern/
---

> Là bản cải tiến của` Module Pattern` trong khi ` Module Pattern` tạo các `public method` chỉ để trả về `private method`, thì `Revealing Module Pattern` chỉ cần map các thuộc tính với các `method private` cần trả về.

***Sample code:***

```js
const myRevealingModule = (function() {
    let privateVar = 'Peter';
    const publicVar = 'Hello World';
    
    function privateFunction() {
        console.log('Name: ' + privateVar);
    }
    
    function publicSetName(name) {
        privateVar = name;
    }
    
    function publicGetName() {
        privateFunction();
    }
    
  /** reveal methods and variables by assigning them to object properties */
    return {
        setName: publicSetName,
        greeting: publicVar,
        getName: publicGetNAme
    };
})();

export default myRevealingModule ;
```
***Use:***

```js
import myRevealingModule from '../Utils/myRevealingModule';
...
myRevealingModule.publicGetName();
...
```

