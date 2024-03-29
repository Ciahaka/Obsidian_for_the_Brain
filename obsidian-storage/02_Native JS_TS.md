[[#callback]] - функция обратного вызова
[[#onChange]]
[[#onClick]] - обработчик событий, принимающий callback.
[event](https://youtu.be/cLxzFhW_dgY?t=1177)  
[addEventListener](https://youtu.be/cLxzFhW_dgY?t=1598)  

[onBlur](https://youtu.be/cLxzFhW_dgY?t=2227)  
[event](https://youtu.be/cLxzFhW_dgY?t=2374)
[[Деструктуризация]]
[Ассоциативный массив](https://www.youtube.com/watch?v=CktBizzHI8g&ab_channel=IT-KAMASUTRA)  - [[#Ассоциативный массив | вниз]]
[Иммутабельность](https://www.youtube.com/watch?v=cONeYnzLccg&ab_channel=IT-KAMASUTRA)
[Иммутабельность в массивах](https://youtu.be/cONeYnzLccg?t=2702)

### callback
[Dimich](https://youtu.be/cLxzFhW_dgY?t=1177)
[Dimich](https://youtu.be/cLxzFhW_dgY?t=156)
Функция которая передаётся параметром(аргументом) в другую функцию.
Функция обратного вызова.

### onChange
[Dimich 06_JS/TS](https://youtu.be/cLxzFhW_dgY?t=1990) 
значением водимом в инпуте всегда строковое. Но, что если стартовое значение стейта числовое?  Все действия с обработчиком события onChange будут ругаться.
Этот момент можно обойти явно задав тип стейту,
```ts
useState<number>(5)
```
и сделав приведение к типу в самом обработчике. 
```ts
onChange = {setState(+e.currentTarget.value)}  /- первый способ
onChange = {setState(Number(e.currentTarget.value))}  /- второй способ			
```

### onClick
[Dimich](https://youtu.be/cLxzFhW_dgY?t=997)
Обработчик события, можно повесить на практически на любой элемент DOM, который может взаимодействовать с пользователем.
В обработчик помещается функция обратного вызова callback.

### Ассоциативный массив
- организационная структура хранения данных. По факту - обычный объект, хранящий в себе массив(ы).
Существует два способа обращения к свойству объекта:
- точечная запись ``user.address.city.title``
- индексная запись ``user['address']['city']['title']``
В ассоциативном массиве мы обращаемся к свойству именно индексной записью, так как ключом свойства может быть любая строк. к которой, впоследствии, нельзя будет обратиться точечной записью.
По сути, все ключи в объектах имеют строковую запись!

Добавляя, при помощи индексной записи, ключи новых свойств в массив/объект, нужно помнить, что независимо от того, передали мы их строкой или нет, они запишутся именно строкой
```js

usersObj[2] = 'число превратилось в строку'  
usersObj[null] = 'null превратился в строку'  
usersObj[{}] = 'объект  превратился в свойство ''[object Object]'''
```
Как проитерироваться по массиву, при условии, что мы не знаем какое количество свойств содержит массив
`Object.keys()`
Статический метод класса Object - keys, вернёт массив всех ключей исходного массива
Похожим образом можно получит значения всех свойств исходного массива
`Object.values()`

В чём + записи данных в ассоциативный массив, в сравнении с обычным массивом?
Создавая асс. массив, мы создаём ключи для каждого его элемента, и достучаться до нужного элемента становиться намного проще. И, при увеличении количества элементов массива, сложность операции по поиску элемента и работы с ним, не увеличивается. 
Сложность алгоритма работы с элементами в асс. массиве всегда равна 
`O(1) - где 1 константа`
Ведь мы обращаемся к элементу напрямую 
`users[3]`.
В отличии от классического массива, где для того, чтобы найти элемент, придётся воспользоваться методом или циклом, который будет искать требуемый ID элемента, при этом итерируя по всем элементам массива, сколь огромен он бы не был!
Сложность алгоритма работы с элементами в массиве всегда равна 
`O(n) - где n - количество эл-ов в массиве`

Создавая новый асс. массив, мы должны создать типизацию для него, в которой скажем, что наш элемент имеет ключ key с типом строка, а значением этого key будет объект(наш элемент)
`[key:string]:{}`
При добавлении нового эл-та в асс. массив исключаются дубликаты.
Удаление эл-та из асс. массива происходит по ключу при помощи ключевого слова `delete`


