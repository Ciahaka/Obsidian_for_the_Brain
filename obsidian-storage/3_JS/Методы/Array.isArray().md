Метод **`Array.isArray()`** возвращает `true`, если объект является массивом и `false`, если он массивом не является. 
	`Array.isArray(obj)` - где obj - проверяемый объект


### [instanceof](obsidian://open?vault=obsidian-storage&file=2_JS%2F%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B) vs isArray

Когда проверяем экземпляр `Array`, `Array.isArray` предпочтительней, чем `instanceof`, потому что он работает и с `iframes`.
