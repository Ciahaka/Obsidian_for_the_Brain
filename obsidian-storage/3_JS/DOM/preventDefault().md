[Mdn Web](https://developer.mozilla.org/ru/docs/Web/API/Event/preventDefault)
[Victor](https://youtu.be/7iKtaKbxNKs?list=PLbLBXDhswD1eA50Kgu2nVUc_MYB3-M7ly&t=6647)
Отменяет событие, в случае если его возможно отменить!  
Метод интерфейса Event, сообщает [[User agent]] , что если событие не обрабатывается явно, то его действие по умолчанию не должно выполняться как обычно.
Событие продолжает выполняться как обычно до тех пор, пока один из обработчиков этого события не вызывает метод [[stopPropagation()]] , который сразу прекращает выполнение(распространение) события.
Вызов метода preventDefault() для события не подлежащего отмене - не имеет смысла! Проверить, является ли событие отменяемым, можно при помощи метода [event.cancelable](https://developer.mozilla.org/en-US/docs/Web/API/Event/cancelable "Currently only available in English (US)")
<b>preventDefault()</b> - не прекращает распространение события! Лишь останавливает (запрещает выполнение).
Для чего?
Например не дать возможность продолжить ввод пользователю, в случае его ошибки. (неверный регистр, неверный язык ввода, недопустимые символы)
Или можно отменить переход по ссылке.
    const a= document.getElementById('a')  
        a.addEventListener('click',(e)=>{  
        e.preventDefault()  
    console.log('stop')  
    })