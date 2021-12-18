---
id: 1639810898255
title: Setup Redux For ReactJs
category: Javascripts/Redux/
---

1. Cài đặt package react-redux và redux

```
npm install --save redux react-redux
```
* Cấu trúc thư mục:

```
src
|__ reducers
| |__ hobby.js
| |__ todo.js
| |__ ... (one reducer per file)
| |__ index.js (root reducer)
|
|__ actions
| |__ hobby.js
| |__ todo.js
| |__ ...
|
|__ pages
| |__ HomePage/index.jsx (connect to redux)
|
|__ store.js (reducers, init state, middlewares)
|__ index.js (setup Store Provider)
```
2. Setup `reducers `và `rootreducer`

```
// reducers/hobby.js
const initialState = {
    list: ['Listening to music'],
    selectedId: null,
}
const hobbyReducer = (state = initialState, action) => {
    switch (action.type) {
        case 'ADD_HOBBY': {
            const newList = [...state.list];
            newList.push(action.payload);
            return {
                ...state,
                list: newList,
            }
        }
        default:
            return state;
    }
};
export default hobbyReducer;
```

```
// reducers/index.js (ROOT)
const rootReducer = combineReducers({
    hobby: hobbyReducer,
})
export default rootReducer;
```
3. Setup redux `store`

```
// src/store.js
const store = createStore(rootReducer);
export default store;
```
4. Setup Store Provider cho toàn app `src/index.js`

```
const Main = () => (
    <Provider store={store}>
        <App />
    </Provider>
)
```
5. Connect vào redux từ reactjs component
* Với `class component`: dùng HOC `connect()`
* Với `functional component`: dùng hooks `useSelector()` và `useDispatch()`

```
function HomePage(props) {
    const hobbyList = useSelector(state => state.hobby.list);
    const dispatch = useDispatch();
    const handleAddHobbyClick = () => {
        const newHobby = 'Coding';
        dispatch({
            type: 'ADD_HOBBY',
            payload: newHobby,
        });
    }
    return ( 
        <div className = "home-page" >
            <HobbyList data={hobbyList}/>
            <button onClick = {handleAddHobbyClick} > Add new hobby </button>
        </div>
    );
}
export default HomePage;
```
---

`Source`: [https://drive.google.com/file/d/1UDDA6F0D7S38P-MxeqwIjCPPD4ITSzCR/view](https://drive.google.com/file/d/1UDDA6F0D7S38P-MxeqwIjCPPD4ITSzCR/view)