Массив (**`Array`**) в JavaScript является глобальным объектом, который используется для создания массивов; которые представляют собой высокоуровневые списко-подобные объекты.
[MDN web docs](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array)
```
'join', 'reverse', 'sort', 'push', 'pop', 'shift', 'unshift',
'splice', 'concat', 'slice', 'indexOf', 'lastIndexOf',
'forEach', 'map', 'reduce', 'reduceRight', 'filter',
'some', 'every'
```
[[map]]
[[filter]]
[[find]]
[[reduce]] - нахождение максимального значения
[[forEach]] - используется для перебора массива.
[[concat]] - объединение массивов
[[includes]] - поиск элемента в массиве
[[push]] - добавление элемента в конец массива
[[split]] - разбивает объект string на массив строк
[[indexOf]] - находит элемент в массиве по его индексу
[[slice]] - обрезает массив по индексу, возвращает новый массив
[[splice]]  добавляет или удаляет элементы из массива,, возвращает массив удалённых элементов
[[#every]] 
[[#some]]
[[join]] - объединяет элементы массива в строку
[[Array.isArray()]] - метод проверяющий объект на массив

#### 

#### every
Метод возвращает true если функция callback подойдёт для каждого элемента массива. Иначе вернёт false
`arr.every(callback[,thisArg])`

#### some
Метод возвращает true если функция callback подойдёт для хотя бы одного элемента массива. Иначе вернёт false
`arr.some(callback[,thisArg])`

