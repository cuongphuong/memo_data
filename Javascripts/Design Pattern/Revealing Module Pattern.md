---
id: 1639736254014
title: Revealing Module Pattern
category: Js/Design Pattern/
---

> Là bản cải tiến của` Module Pattern` trong khi ` Module Pattern` tạo các `public method` chỉ để trả về `private method`, thì `Revealing Module Pattern` chỉ cần map các thuộc tính với các `method private` cần trả về.

*Sample code:*

```
const my RevealingModule = (function() {
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

myRevealingModule.setName('Mark');

// prints Name: Mark
myRevealingModule.getName();
```
