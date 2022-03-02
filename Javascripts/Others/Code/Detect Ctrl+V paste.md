---
id: 1646231703817
title: Detect Ctrl+V paste
category: Javascripts/Others/Code/
---


```
document.body.addEventListener("keydown", function (ev) {
  
    // function to check the detection
    ev = ev || window.event;  // Event object 'ev'
    var key = ev.which || ev.keyCode; // Detecting keyCode
      
    // Detecting Ctrl
    var ctrl = ev.ctrlKey ? ev.ctrlKey : ((key === 17)
        ? true : false);
  
    // If key pressed is V and if ctrl is true.
    if (key == 86 && ctrl) {
        // print in console.
        console.log("Ctrl+V is pressed.");
    }
    else if (key == 67 && ctrl) {
  
        // If key pressed is C and if ctrl is true.
        // print in console.
        console.log("Ctrl+C is pressed.");
    }
  
}, false);
```
