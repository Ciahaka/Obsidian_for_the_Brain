[MDN Web](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
[Learn JS](https://learn.javascript.ru/array-iteration#foreach)

Метод массива **`forEach()`** выполняет указанную функцию один раз для каждого элемента в массиве.
Не возвращает новый массив, возвращает [`undefined`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/undefined)

Метод `forEach()` выполняет функцию `callback` один раз для каждого элемента, находящегося в массиве в порядке возрастания. Она не будет вызвана для удалённых или пропущенных элементов массива. Однако, она будет вызвана для элементов, которые присутствуют в массиве и имеют значение [`undefined`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/undefined).

```js
arr.forEach(function callback(currentValue, index, array) {
    //your iterator
}[, thisArg]);
```
```js

var arr = ["Яблоко", "Апельсин", "Груша"]; arr.forEach(function(item, i, arr) { alert( i + ": " + item + " (массив:" + arr + ")" ); });
`callback`  //0: Яблоко (массив:Яблоко,Апельсин,Груша)
```

Функция, которая будет вызвана для каждого элемента массива. Она принимает от одного до трёх аргументов:

`currentValue`
Текущий обрабатываемый элемент в массиве.

`index` Необязательный
Индекс текущего обрабатываемого элемента в массиве.

`array` Необязательный
Массив, по которому осуществляется проход.

`thisArg`
Необязательный параметр. Значение, используемое в качестве `this` при вызове функции `callback`.

! Не существует способа остановить или прервать цикл `forEach()` кроме как выбрасыванием исключения !