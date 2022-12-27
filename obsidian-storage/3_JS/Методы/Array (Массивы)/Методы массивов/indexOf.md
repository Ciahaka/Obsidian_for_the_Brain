[Mdn Web](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
[IndexOf под капотом](https://youtu.be/kY6g2ofO_Qg?list=PLbLBXDhswD1ebx1pf31nXbW3VauIzAm3v&t=5141)

Метод массива indexOf возвращает первый индекс, по которому элемент может быть найден в массиве. Или же, возвращает -1 , если такого индекса нет в массиве
```javascript

const indexOffGlobal =(array, num) => {
  for(let i = 0; i < array.length; i++){
    if(array[i] === num) {
      return i
    }
 }
return -1
}
```
1. В нашу функцию приходит два параметра. сам исходный массив и некое число (искомый индекс элемента).
2. Поскольку, в случае отсутствия нужного индекса в массиве, indexOf возвращает -1, то и нам нужно ретурнуть тот же -1.
3. Создаём цикл [[for]], который пробежит по элементам исходного массива и в случае совпадения индекса элемента в массиве и искомого индекса - ретурнет этот индекс(элемент)