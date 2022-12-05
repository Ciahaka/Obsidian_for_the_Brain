[Mdn Web](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
[Find под капотом](https://youtu.be/kY6g2ofO_Qg?list=PLbLBXDhswD1ebx1pf31nXbW3VauIzAm3v&t=3556)
Метод массива find применят переданую функцию callback один раз для каждого, присутствующего в исходном массиве элемента, до тех пор пока она не вернёт true. Как только такой элемент массива найден , метод find возвращает этот элемент (его значение)
<h4>Метод find под капотом</h4>
const findGlobal = (array, func) => {
   for(let i = 0; i < array.length; i ++) {
       if(func(array[i]) === true) {
           return array[i]
       }
   }
}

1. Метод массива find не создаёт и не возвращает новый массив. 
2. Функция получает в параметрах некий исходный массив и callback функцию, которая будет применться к элементам исходного массива.
3. Внутри функции создаём цикл [[for]], который пробежит по всем элементам  массива, применяя для каждого из них callback функцию func, и в случае результата true, просто ретурнет этот элемент массива.