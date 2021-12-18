---
id: 1639847747724
title: useEffect()
category: Javascripts/ReactJS/Hooks/
---

`useEffect() `để quản lý vòng đời của của một component và nó phục vụ chúng ta sử dụng trong `function component` thay vì các `lifecycle `như trước đây trong `class component.`

* `useEffect `cho phép chúng ta sử lý `logic `trong `lifecycle methods`. (`componentDidMount()`)
* Hàm sẽ được gọi mỗi khi có gì đó ảnh hưởng đến `state ` trong components. (`componentDidUpdate ()`)
* Hàm có `function cleanup` chạy mỗi khi `component unmount `(`componentWillUnmount()`)


```
  useEffect(() => {
    // ~componentDidMount(), componentDidUpdate()
    ...
    // return 1 function, sẽ được gọi ngay trước khi componentWillUnmount
    return () => {
      // clear data, sử lý trước khi unmount component
    }
  }, []); // Danh sách các state dependence (useEffect sẽ thực khi khi các state này phát sinh thay đổi)
```
