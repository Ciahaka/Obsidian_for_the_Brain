[Create React App Doc](https://create-react-app.dev/)
1. Выбрать директорию, в которой будет размещаться проект.
2. Правой клавишей мыши вызываем Git Bash Here
3. Прописываем в консоли Git Bash Here команду
         yarn create react-app my-app --template typescript
         [Adding TS](https://create-react-app.dev/docs/adding-typescript)
    Где my-app меняем на имя нашего проекта.
4. Открываем проект через WS 
5. В консоли WS вводим 
        yarn start
6. В дереве проекта находим файл '.gitignore'  и прописываем туда папку 
        '/.idea'
7. Коммитим изменения, но не пушим.
8. Переходим на GitHub, создаём  новый репозиторий под проект.
9. В директории проекта вызываем Git Bash Here
10. Проверяем скрытые папки на наличие папки '! git' . По умолчанию обычно присутствует
11. Вводим команды в консоли Git Bash
        git branch -M main
        git remote add origin ….
        git push -u origin main
Команды лежат во вновь созданном репозитории
12. Обновляем страницу GitHub и проверяем наличие папки idea.
13. Если вдруг есть, то удаляем. Удаление с GitHub, без локального удаления происходит по команде, прописанной в терминале WS
      git rm -r --cached .idea
14. Коммитим и пушим.
#create
