---
id: 1639736525759
title: React Hooks useMemo()test
category: React Hooks/
---

useMemo cũng giống như khái niệm `React memo`, nhưng có sự khác biệt rõ ràng. Nếu như `React memo` sinh ra với mục địch tránh việc rerender nhiều lần thì `useMemo `tránh cho việc tính toán lại một function lặp đi lặp lại nhiều lần mỗi lần component re-render khi thay đổi các `state `không liên quan.

**Sample:**
```
export default function Test() {
    const [nunm, setNunm] = useState(0);
    const result = useMemo(() => function () {
        // 3s proccessing
        return nunm + 1;
    }, [nunm]);

    return (
        <div>
            <p>Number: {result}</p>
        </div>
    )
}

```
