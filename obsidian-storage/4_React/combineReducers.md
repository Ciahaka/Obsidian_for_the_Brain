[reactdev](https://reactdev.ru/libs/redux/api/combineReducers/)
[Dimich](https://www.youtube.com/watch?v=5Ei5nru5Ly4&ab_channel=IT-INCUBATOR)
```js
combineReducers(reducers);
```
 Эта функция возвращает новый reducer (рутовый reducer)
 ```js
 const x = combineReducers(
   {
     a: Reducer_1,
     b: Reducer_2,
     c: Reducer_3,
   }
 )
```