[MDN Web](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
Метод **`slice()`** возвращает новый массив, содержащий копию части исходного массива.
`begin` Необязательный

Индекс (счёт начинается с нуля), по которому начинать извлечение.

Если индекс отрицательный, `begin` указывает смещение от конца последовательности. Вызов `slice(-2)` извлечёт два последних элемента последовательности.

Если `begin` не определён, `slice()` начинает работать с индекса `0`.

Если `begin` больше длины последовательности вернётся пустой массив.

`end` Необязательный

Индекс (счёт начинается с нуля), по которому заканчивать извлечение. Метод `slice()` извлекает элементы с индексом меньше `end`.

Вызов `slice(1, 4)` извлечёт элементы со второго по четвёртый (элементы по индексам 1, 2 и 3).

Если индекс отрицательный, `end` указывает смещение от конца последовательности. Вызов `slice(2, -1)` извлечёт из последовательности элементы начиная с третьего элемента с начала и заканчивая вторым с конца.

Если `end` опущен, `slice()` извлекает все элементы до конца последовательности (`arr.length`).
!!Возвращает новый массив, содержащий извлечённые элементы. Не мутирует исходный массив!!
