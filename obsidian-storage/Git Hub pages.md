1. В файле package.json проекта прописываем домашнюю страницу 
   своего проекта и имя проекта
        ''name'': ''имя проекта''
        "homepage": "https://Chiahaka.github.io/ имя проекта"
2. В терминале WS прописываем команду
        yarn add gh-pages
3. В файле package.json, в объект "scripts" нужно добавить команды, при условии, что их там нет
        "predeploy": "npm run build"
        "deploy": "gh-pages -d build" 
4. В терминале WS прописываем команду
        yarn run deploy

Возмоные ошибки