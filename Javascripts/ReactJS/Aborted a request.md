---
id: 1647837718244
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
        let htmlMd = await markdown(source.content, signal);
        if (!signal.aborted) {
            setContent(htmlMd);
        }
    }
}
```
