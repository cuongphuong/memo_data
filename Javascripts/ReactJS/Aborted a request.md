---
id: 1647835933377
title: Aborted a request
category: Javascripts/ReactJS/
---



```js
function QuickSearchTab(props) {
    // use for control sync process
    const refController = React.useRef(null);

    useEffect(() => {
        // Code

        return () => {
            refController.current.abort();
        }
    }

    async function doneTyping(keyword) {
        refController.current = new AbortController();
        let signal = refController.current.signal;
        // fetch API
        let apiResultContentList = await ContentRender.search(keyword, signal);
    }
}
```
