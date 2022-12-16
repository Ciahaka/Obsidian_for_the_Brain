```ts

	 import React from 'react';  
  
    export type ButtonType = {  
      name: string                <<--- "у любой кнопки есть имя"
      callback: () => void        <<--- "в любую кнопку приходит callback"
    }  
  
    export const Button = (props: ButtonType) => {  
       const {name, callback} = props           <<--- "деструктуризация типа"
       const onClickButtonHandler = () => {  
       props.callback()  
    }  
    return(  
      <button onClick={onClickButtonHandler}>{props.name}</button>  
     );  
    };

#button
```