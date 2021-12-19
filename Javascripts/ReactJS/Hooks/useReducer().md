---
id: 1639925724006
title: useReducer()
category: Javascripts/ReactJS/Hooks/
---


```
const dataFetchReducer = (state, action) => {
  switch (action.type) {
    case "FETCH_INIT":
      return {
        ...state,
        isLoading: true,
        isError: false
      };
    case "FETCH_SUCCESS":
      return {
        ...state,
        isLoading: false,
        isError: false,
        data: action.payload
      };
    case "FETCH_FAILURE":
      return {
        ...state,
        isLoading: false,
        isError: true
      };
    default:
      throw new Error();
  }
};

function App() {
  const [state, dispatch] = useReducer(dataFetchReducer, {
    data: [],
    isLoading: false,
    isError: false
  });

  useEffect(() => {
    getData();
  }, []);

  const getData = () => {
    dispatch({ type: "FETCH_INIT" });
    callingAPI()
      .then(res => {
        dispatch({ type: "FETCH_SUCCESS", payload: res });
      })
      .catch(error => {
        dispatch({ type: "FETCH_FAILURE" });
      });
  };

  return (
    <div className="App">
      {state.data.map(item => (
        <Item />
      ))}
      {state.isLoading && <Loading />}
      {state.isError && <Error />}
    </div>
  );
}
```
* useState:

```
A) JavaScript primitives as state (state là các kiểu dữ liệu cấu trúc sơ khai(undefined, boolean, number, string, bigInt, Symbol)
B) simple state transitions (các cái thay đổi thay đơn giản)
C) business logic within your component (code logic ở trong component luôn)
D) different properties that don't change in any correlated way and can be managed by multiple useState hooks (các state khác nhau không phụ thuộc lẫn nhau và có thể quản lí bằng nhiều useState riêng biệt)
E) state co-located to your component (các state dính kèm với component, cái này ví dụ như là hàm onChange của Input nè)
F) a small application (but the lines are blurry here)
```

* useReducer

```
A) JavaScript objects or arrays as state (state là object hoặc array)
B) complex state transitions (các thay đổi state phức tạp hơn)
C) complicated business logic more suitable for a reducer function (có business logic phức tạp thì nên bỏ logic vô reducer để tập trung lại một chỗ)
D) different properties tied together that should be managed in one state object (các state liên quan/ phụ thuộc lẫn nhau thì nên được quản lí bằng một state object)
E) the need to update state deep down in your component tree
F) a medium-sized application (NB: the lines are blurry here)
G) need for an easier time testing it
H) need for a more predictable and maintainable state architecture (cái này thì quá dễ thấy rồi)
```

