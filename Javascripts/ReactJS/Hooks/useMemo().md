---
id: 1639846893428
title: useMemo()
category: Javascripts/ReactJS/Hooks/
---

`useMemo `cũng giống như khái niệm `React memo`, nhưng có sự khác biệt rõ ràng. Nếu như `React memo` sinh ra với mục địch tránh việc rerender nhiều lần thì `useMemo `tránh cho việc tính toán lại một function lặp đi lặp lại nhiều lần mỗi lần component re-render khi thay đổi các `state `không liên quan.

* Tránh `re-reder` các function không cần thiết 
* `useMemo` tập trung vào việc tránh lặp đi lặp lại các logic tính toán nặng nề.

***Sample:***
```
export default function Test() {
    const [nunm, setNunm] = useState(0);
    // Là function có sử lý phức tạp và không liên quan đến các state thay đổi khác -> không cần re-render khi các state khác thay đổi
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
