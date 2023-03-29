[reactdev](https://reactdev.ru/libs/redux/api/combineReducers/)
[Dimich](https://www.youtube.com/watch?v=5Ei5nru5Ly4&ab_channel=IT-INCUBATOR)
При разрастании приложения появляется необходимость разделить функцию редьюсер на отдельные функции, который будут управлять отдельными частями состояния приложения.
Функция combineReducers преобразует объект, свойствами которого являются отдельные функции редьюсер, в одну функцию редьюсер, которая передаётся в createStore.
```js
combineReducers(reducers);
```
 `reducers` (_Object_) - объект, значения которого соответствуют различным функциям редьюсерам, которые должны быть объединены в один. 
 
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

х - это обычный reducer (рутовый reducer), который мы закидываем в createStore.
Когда диспатчим action, они попадают в рутовый reducer, туда же попадает весь state. Далее рутовый reducer забрасывает всё это в combineReducers, тот в свою очередь распределяет всё по своим св-вам ( которые являются reducer, отвечающими за отдельную часть логики), запуская их.
Декомпозиция reducer ???
Типизация рутового reducer: ReturnType 
 