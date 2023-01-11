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

Св-во `justify-content` hfcghtltkztn ''