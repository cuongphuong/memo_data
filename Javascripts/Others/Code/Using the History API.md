---
id: 1646471519259
title: Using the History API
category: Javascripts/Others/Code/
---

The HTML5 History API is definitely the way to go for modern websites. It accomplishes the task at hand, while also providing additional functionality. You can use either `history.pushState()` or `history.replaceState(`) to modify the URL in the browser, depending on your needs:

```
// Current URL: https://my-website.com/page_a
const nextURL = 'https://my-website.com/page_b';
const nextTitle = 'My new page title';
const nextState = { additionalInformation: 'Updated the URL with JS' };

// This will create a new entry in the browser's history, without reloading
window.history.pushState(nextState, nextTitle, nextURL);

// This will replace the current entry in the browser's history, without reloading
window.history.replaceState(nextState, nextTitle, nextURL);
```

Source: [https://www.30secondsofcode.org/articles/s/javascript-modify-url-without-reload]()
