Оператор, который проверяет принадлежность объекта к определённому классу или его родителю.
Или же...
`instanceof` проверяет, присутствует ли объект `constructor.prototype` в цепочке прототипов `object`
```
    object instanceof constructor
```
`object`
Проверяемый объект.
`constructor`
Функция-конструктор, на которую идёт проверка.

```
// объявляем конструкторы
function C() {}
function D() {}

var o = new C();

// true, так как: Object.getPrototypeOf(o) === C.prototype
o instanceof C;

// false, так как D.prototype не присутствует в цепочке прототипов o
o instanceof D;
```
Результат оператора `instanceof` зависит от свойства `constructor.prototype`