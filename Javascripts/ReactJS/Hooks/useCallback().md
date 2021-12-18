---
id: 1639846666172
title: useCallback()
category: Javascripts/ReactJS/Hooks/
---

`useCallback `là được sử dụng để tối ưu quá trình render của `React functional components`

* Tránh việc re-render `component con` khi nhận 1 function từ `component cha` làm `depedence `trong `useEffect()`
* Sử dụng khi muốn truyền 1 `function `từ `component cha` vào `component con`

***Example:***

```
const Child = ({ someFunc }) => {
    useEffect(() => {
        someFunc();
        ...
    }, [someFunc]); // Function truyền từ cha được import vào dependence -> sẽ re-render component khi function này thay đổi địa chỉ
    return <> </>
};

const App = () => {
    // Function được truyền làm props cho function con, sẽ bị thay đổi địa chỉ khi function cha re-render
    const plusFive = useCallback(() => {
        ...
    }, [num]);

    return (
        <Child someFunc = {plusFive}/>
    );
}
```

***Note:***

1. Chỉ sử dụng khi thực sự cần, vd giảm hiểu suất khi không sử dụng.
2. Việc lạm dụng làm cho các version cũ của fuction lưu lại trong bộ nhớ -> giảm hiệu suất, khả năng hoạt động sai khi đọc lại các function cũ.