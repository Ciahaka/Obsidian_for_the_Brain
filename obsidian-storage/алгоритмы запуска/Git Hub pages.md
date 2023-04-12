1. В файле package.json проекта прописываем домашнюю страницу 
   своего проекта и имя проекта
        ''name'': ''имя проекта''
        "homepage": ""https://Ciahaka.github.io/DZ_Avto -(имя проекта)"
2. В терминале WS прописываем команду
        yarn add gh-pages
3. В файле package.json, в объект "scripts" нужно добавить команды, при условии, что их там нет
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build" 
4. В терминале WS прописываем команду
        yarn run deploy

Возможные ошибки:
- ошибка 404  при переходе на страницу git hub pages - нужно подождать и обновить страницу (для деплоя нужно время) 
- отображается readme файл  при переходе на страницу git hub pages - на git hub странице репозитория изменить в настройках ветку main на gh-pages branch