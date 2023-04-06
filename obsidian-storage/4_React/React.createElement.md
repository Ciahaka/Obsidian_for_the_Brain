Этот метод, в отличии от классического JS метода `document.createElement`(не используется в React), возвращает не DOM элемент, а объект представляющий этот DOM элемент.
```js
const element = React.createElement("h1");
//возвращает объект, подобный этому:
{
  type: 'h1',
  props: {}
}
```
Это происходит из-за того, что React работает с виртуальным DOM.(оптимизация)
Назначение атрибутов возвращаемому элементу происходит следующим образом
```js
React.createElement("h1", {className: "center", style: "color: red"})
```

Ниже необходимые импорты и методы для отрисовки элемента  в заданный элемент `<div id={'root'}></div>`  в index файле
```js
import React from 'react';
import {createRoot} from "react-dom/client";  
  
const root = document.querySelector("#react-root");  
createRoot(root).render(React.createElement("p", {}, "Hello World"));
```
или
```js
import React from 'react'
import {createRoot} from "react-dom/client";

const root  = document.getElementById("react-root")
createRoot(root).render(React.createElement('h1',{className:"title"},'Online Supermarket'))
```