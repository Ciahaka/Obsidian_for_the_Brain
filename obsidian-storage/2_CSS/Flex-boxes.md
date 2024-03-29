[Шпаргалка](https://tpverstak.ru/flex-cheatsheet/)
1. Определяем есть ли родитель у эл-ов, которые нужно позиционировать.
    Практически все свойства флексов будут применяться к родителю.
    ! Родитель управляет детьми!
2. Задаётся в стилях родителя свойство  `display` - определяет как именно должен быть показан элемент.
   `: flex` - Элемент внутри ведёт себя как блочный.
   `inline-flex` - Элемент ведёт себя как строчный
3. Как только прописали свойство `display`, сразу установился набор свойств по умолчанию, для вложенных элементов.
```js
flex-direction: row;
flex-wrap: nowrap;
justify-content:flex-start;
align-items: flex-start;
align-content: stretch;
flex-grow: 0;
flex-shrink: 1;
flex-basis: auto;
align-self:auto
```

Св-во `justify-content` распределяет эл-ты по оси указанной в свойстве `flex-direction: row;` (по главной оси)
Св-во `align-content` располагает эл-ты по второстепенной оси.
! Свойства флексов распространяются только на вложенные элементы родителя. Если у этих же элементов тоже есть вложенность, то флексы не будут работать внутри !
Стандарт ширины экрана 1140-1200px.  Данную ширину задаёт `container`.
4. Если на макете видно, что все элементы прижимаются к невидимой границе, то это точно контейнер.
   Как определить размер контейнера?
- Смотрим на макете заданную ширину экрана. 
- Находим на макете элемент максимально выдающийся к краю.
- Определяем сколько пикселей от края нашего элемента до края экрана.
- Повторяем всё тоже самое для аналогичного элемента с другой стороны.
- Суммируем эти значения и эту сумму вычитаем из ширины экрана. так и получим размер контейнера.
Стили для класса контейнера задаются в самом верху файла, под звёздочкой
Класс контейнера  - универсален, и может использоваться как модуль из проекта в проект!
```js
.container {  
    max-width: 1170px;  
    width: 100%;  
    height: 100%;  
    padding: 0 15px;  
    margin: 0 auto;
}
```

`max-width` - для адаптивности ресурса. Поэтому ширину делаем гибкой, но не более заданного значения.
`width` - дополнительно задаём, со значением 100%. Это позволит подстраиваться ресурсу под сильное уменьшение экрана. Например для мобильных устройств.
`height: 100%;` аналогично
`padding: 0 15px;` - заранее предусматриваем отступы для экранов мобильных устройств. Этот шаг уменьшает свободное пространство внутри контейнера на 30px. Элементам внутри может стать тесно. Поэтому, сразу добавим эти 30px к существующим пикселям в свойстве `max-width`. Компенсируем!
`margin: 0 auto;` - выравниваем контейнер по центру.
На этом этапе можно добавить яркий `border`, с ним будет проще работать с пустым пространством.
5. Класс контейнера подключается в HTML не в теги секций, а внутри них создаётся `div` с классом. которая оборачивает элементы секции.
6. Как правило, если к этому моменту свёрстано и застилизованно, то всё поломается. Произошло это потому-что во всех тегах со стилями, дочерним элементом стал контейнер. чтобы обойти эту проблему существует класс-обёртка `wrap`
7. Дивка с данным классом помещается в дивку с контейнером  и в неё оборачиваются элементы. В файле стилей, в соответствующий класс пишутся(или переносятся) свойства отвечающие за позиционирование эл-ов. Имя класса врапера лучше задавать соответственно имени тега, в котором всё происходит
8. Дополнительным свойством враперу нужно задать высоту со значением 100%.


### Свойства применяемые к контейнеру:

`flex-direction` - задает направление главной оси  (по умолчанию - row)
   - row - элементы размещаются по направлению текста.
   - wrap - элементы автоматически переносятся на новую строку.
   - wrap-reverse - Элементы автоматически переносятся на новую строку, но строки расположены в обратном порядке.

---

### Свойства применяемые к отдельному элементу внутри контейнера:
`order` - определяет порядок элемента. Каким по счету (в ряду или столбце) он будет 
   Значения: 1, 2, 3…
`align-self` - выравнивает 1 элемент (ребенка) по второстепенной оси (если нужно его как-то по-другому разместить)

