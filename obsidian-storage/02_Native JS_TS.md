[callback](https://youtu.be/cLxzFhW_dgY?t=1177)  
[onClick](https://youtu.be/cLxzFhW_dgY?t=997)  
[event](https://youtu.be/cLxzFhW_dgY?t=1177)  
[addEventListener](https://youtu.be/cLxzFhW_dgY?t=1598)  
[onChange](https://youtu.be/cLxzFhW_dgY?t=1990)  
[onBlur](https://youtu.be/cLxzFhW_dgY?t=2227)  
[event](https://youtu.be/cLxzFhW_dgY?t=2374)
[[Деструктуризация]]
[Ассоциативный массив](https://www.youtube.com/watch?v=CktBizzHI8g&ab_channel=IT-KAMASUTRA) 

Ассоциативный массив - организационная структура хранения данных. По факту - обычный объект, хранящий в себе массив(ы).
Существует два способа обращения к свойству объекта:
- точечная запись user.address.city.title
- индексная запись user['address']['city']['title']
В ассоциативном массиве мы обращаемся к свойству именно индексной записью, так как ключом свойства может быть любая строк. к которой, впоследствии, нельзя будет обратиться точечной записью.
По сути, все ключи в объектах имеют строковую запись!

Как проитерироваться по массиву, при условии, что мы не знаем какое количество свойств содержит массив
    Object.keys()
Статический метод класса Object - keys, вернёт массив всех ключей исходного массива