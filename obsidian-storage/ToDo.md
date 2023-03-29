[[#метод "map" **13:52**]]

## 01_02 - TodoList for students
[Dimich](https://samurai.it-incubator.io/pc/video-content/watch/60b5104ef084890015872dbe)
#### Метод "map" **13:52** 
Для прохода по массиву тасок используем метод map. 
Внутри ul обращаемся к приходящему в props массиву тасок посредством map.
!!! Нужно помнить , что это уже JSX и поэтому весь блок кода оборачиваем фигурными скобками!!!
Коллбэк в map типизируем как TasksType (если тип задан, то сама ide подскажет).
 Помещаем одну из li в return map. 
 !!! В метода map в обязательном порядке указываем атрибут key для возвращаемого элемента. Это поможет React работать эффективно при итерации по массиву и при добавлении или удалении элементов из массива. Без атрибута key react может работать некорректно. 
 Подробно об [key](obsidian://open?vault=obsidian-storage&file=4_React%2FReact)  !!! 
 В самой li уже обращаемся не через props  (поскольку сам метод map уже в props), а напрямую к итерируемому элементу массива.
 Остальные li можно удалять.
#### Удаление задач/onClick 19:03
Добавляем button внутрь отрисовываемой map li.
На button вешаем обработчик события onClick.
!!! Помним, что в onClick помещаем функцию callback которая будет вызываться при  нажатии на кнопку. Не забываем про `()=>{}`!!!





**30:10** -функция для удаления задачи
**41:19** - фильтрация массива с task'ами
**43:06** - Local State (useState)
**1:04:21** - фильтрация задач (all | active | completed)
**1:18:54** - ИТОГ

## 03 - TodoList for students
[[#UUID]] - Подключение uuid к проекту
[7:48](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=468s) - про key
[9:18](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=558s) - addTask
[17:05](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=1025s) - чтение значения из input
[29:13](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=1753s) - очистка поля input (onChange)
[30:09](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=1809s) - добавление task при нажатии на enter (onKeyPress)
[37:51](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=2271s) - рефактор кода
[47:37](https://www.youtube.com/watch?v=jh2XvRX7fw4&t=2857s) - рефактор функции удаления
[9:01](https://youtu.be/ut7SbOKilZE) – Aктивный чекбокс
[32:10](https://youtu.be/ut7SbOKilZE?t=1935) – trim() Убрать пробелы и пустые строки
[39:00](https://youtu.be/ut7SbOKilZE?t=2347) – title is required. Ошибка пустого ввода
[47:50](https://youtu.be/ut7SbOKilZE?t=2902) – подсветка кнопок выполненных тасок
[53:54](https://youtu.be/ut7SbOKilZE?t=3114) - затенение выполненных тасок
[12:00](https://www.youtube.com/watch?v=mF6NfolktTY&t=720s) – массив todolists
[16:20](https://www.youtube.com/watch?v=mF6NfolktTY&t=980s) – фильтрация тасок для каждого todolist
[18:49](https://youtu.be/mF6NfolktTY?t=1131) - коррекция функции изменения фильтра

[23:52](https://youtu.be/mF6NfolktTY?t=1432) - помещаем переменную с тудулистами в useState
[24:29](https://youtu.be/mF6NfolktTY?t=1495) - модифицируем функцию изменения фильтра  
[29:00](https://www.youtube.com/watch?v=mF6NfolktTY&t=1740s) – где хранить таски
[37:39](https://youtu.be/mF6NfolktTY?t=2272) - чиним функции над return
[44:45](https://www.youtube.com/watch?v=mF6NfolktTY&t=2685s) – debugger
[47:00](https://www.youtube.com/watch?v=mF6NfolktTY&t=2820s) – удаление todolists
[49:40](https://www.youtube.com/watch?v=mF6NfolktTY&t=2980s) – удаление todolist tasks из стейта
[1:00](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=60s), [2:40](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=160s) – переиспользование input
[13:30](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=810s) – обертка addTask
[18:30](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=1110s) – добавляем новый todolist
[21:00](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=1260s) – типизация tasksObj

[28:20](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=1700s) – редактирование span
[32:16](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=1936s) – EditableSpan
[53:30](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=3210s) – редактирование todolist name
[58:00](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=3480s) – debugger (как работает editable span)
[59:40](https://www.youtube.com/watch?v=Q-TPmODeF2M&t=3580s) – резюме (рисовалка)
## material-ui
[20:00](https://www.youtube.com/watch?v=zNbqQty3O1Q&t=1200s) – кнопки
[23:40](https://www.youtube.com/watch?v=zNbqQty3O1Q&t=1420s) – инпут
[31:35](https://www.youtube.com/watch?v=zNbqQty3O1Q&t=1895s) – чекбокс
[44:30](https://www.youtube.com/watch?v=zNbqQty3O1Q&t=2670s) – AppBar
[47:10](https://www.youtube.com/watch?v=zNbqQty3O1Q&t=2830s) – Container, grid
## reducer
[8:00](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=480s) – как работает reducer 
[10:00](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=600s) – начало. игрушечные тесты
[19:00](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=1140s) – тесты для reducer
[26:30](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=1590s) – иммутабельность для редьюсера
[30:30](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=1830s) – TDD (test-driven development)
[38:10](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=2290s) – reducers for todolists
[40:30](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=2430s) – тесты для todolist reducers
[58:40](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=3520s) – типизация actions
[1:07:00](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=4020s) – action creators
[1:18:30](https://www.youtube.com/watch?v=5AeVQOpvYEA&t=4710s) – debugger
## Reducer for tasks [Клац](https://samurai.it-incubator.ru/pc/video-content/watch/60b52128f084890015872df5)
**14:40** – начало  
**21:40** – тесты
31:35 - добавление таски
56:37 - стейт тасок при добавлении тудулиста
1:00:00 - объяснение структуры теста

Удаление тасок
#Удаление_тасок


Фильтрация состояния тасок
#фильтрация_тасок

### UUID
[Dimich](https://samurai.it-incubator.ru/pc/video-content/watch/60b510c6f084890015872dbf)
UUID - библиотека, которая генерирует текстовые, уникальные id
Подключение к проекту
```ts
yarn add uuid
yarn add @types/uuid
```
``

