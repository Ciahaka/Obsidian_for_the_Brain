[[#Команды]]
[[#Отмена commit]]
[[#Удаление commit]]
[[#Переименовать commit]]
[[#Изменить содержание commit]]
[[#Откат последних изменений]]
[[#Удаление папок и файлов с удалённого репо]]
[[#Удаление commit с удалённого репозитория]]
[[#Клонирование удалённого репозитория. Колобараторы]]
[[#Pull request]] - подробно
[[#Branch или Ветки проекта]]
[[#Разрешение конфликтов в WS]]
[[#Git Stash / Unstash]] - временное хранилище участков кода
[[#Локальная история Git]] - восстановить несохраненные данные
[[#Github Gist]] - хранение пере-используемой логики
[[#Несколько учёток Github на одной машине]]

Система для контроля, отслеживания и ведения истории изменения файлов в проекте. При помощи Git  можно откатить свой проект до более старой версии, сравнивать, анализировать и сливать свои изменения в [[repository]] (репозиторий).
Git работает локально и все репозитории хранятся на жёстком диске. репозитории можно хранить и в сети, для этого используют ресурс [[Github]].
Каждая точка сохранения проекта называется [[commit]] (коммит). Из множества подобных commit-ов собирается [[branch]] (ветка)

Команды забиваются в панели gitbush локального репозитория git
## Команды
`git clone + путь к репозиторию` - позволяет клонировать к себе удалённый репозиторий. путь можно указать при помощи индификаторов SSH или воспользовавшись ссылкой HTTPS

`git status`  - покажет состояние текущего локального репозитория. Наличие ошибок, рекомендации.

`git add + путь к файлу(наименование файла)`  - позволяет добавить созданный файл (добавленный в папку) в локальное git хранилище и git может производить манипуляции с этим файлом

`git commit -am'add new file'`-  сохранение(фиксация) изменения файла в локальном репозитории + комментарий `ctrl +K` - горячие для WS

`git push` - отправляет изменение на удалённый репозиторий, например github. `ctrl + shift +K` горячие клавиши

`git pull` - позволяет забрать изменения с удалённого репозитория к себе в локальный. В WS есть синяя галка Update Project


### Отмена commit
В панели git WS выбираем нужный commit, правой клавишей кликаем на нём и находим команду `Revert Commit`. Тем же самым действием можно вернуть отменённый commit на место

### Удаление commit
В панели git WS выбираем нужный commit, правой клавишей кликаем на нём и находим команду `Reset Curent Branch..`  Появится диалоговое окно , в котором будет предложено несколько вариантов удаления коммитов.
- Hard - удалит все последние commit за выбранным  commit и из локального репозитория и из удалённого репозитория
- 

### Переименовать commit
В панели git WS выбираем нужный commit, правой клавишей кликаем на нём и находим `Edit Commit message` В открывшемся окне меняем название commit

### Изменить содержание commit
Можно добавить файл в уже отправленный commit. Для этого на вкладке добавления commit нужно воспользоваться командой `Amend Commit` данная команда добавит файл в предыдущий ? commit

### Откат последних изменений
`alt + ctrl + Z` - вызовет диалоговое окно, в котором можно чекнуть в каких именно файлах нужно откатить последние изменения

### Удаление папок и файлов с удалённого репо
Удаление папки
```js
git rm -r --cached .idea
```

Удаление файла
```js
git rm имя файла
```

### Удаление commit с удалённого репозитория
```js
git reset --hard HEAD^^ -//??? нужно ли прописывать hash?
git push -f  - //завершает процесс, убирая комиты с локала и удалёного репо
```
Удаляет всю ветку от узла commit к которому нужно вернуться. Как удалить один commit не удаляя всю ветку?

### Клонирование удалённого репозитория. Колобараторы
Рассмотрим случай, когда над одним репозиторием работает несколько человек, и для каждого для них нужны права на commit и push.
Ссылку для клонирования можно взять в репозитории, во вкладке `Code`. Рекомендуется использовать SSH ссылку, но можно воспользоваться и HTTPS
![[Pasted image 20230219221027.png]]
После, в папке предполагаемого проекта, вызываем консоль Git Bush Here и прописываем команду 
`git clone + путь к репозиторию` + enter
Для того, чтобы дать права на push кому-то ещё, нужно зайти в настройки (шестерёнка) на странице репозитория, найти вкладку `Collaborators`, нажать `Add people` и найти нужного человека по юзернейму. На почту колобаранту упадёт приглашение, приняв которое он получит права на push.

### Pull request
Эта команда позволяет стороннему разработчику предложить улучшение вашего кода, исправить багу, какм-либо образом влиять на ваш проект.
Имея доступ к вашему удалённому репозиторию, стороннему разработчику первым делом нужно форкнуть(вилка, раздвоение, развилка) этот репозиторий
![[Pasted image 20230219224259.png]]
Это действие создаст аналогичный репозиторий в его профиле. Далее он сможет вносить изменения в код, клонируя его себе в локалку. При таком раскладе все изменения пушаться не в репозиторий создателя, а в форкнутый репозиторий стороннего разработчика.
Чтобы отправить все изменения с репозитория стороннего разработчика в наш репозиторий, нужно использовать команду `pull request`
Создать `pull request` можно через вкладку  Git --> GitHub --> Create Pull Request в WS
Или на странице форкнутого репозитория войти во вкладку `Pull Request` и в диалоговом окне кликнуть на `Create а Pull Request`. Далее нужно выбрать откуда и куда нужно отправить изменения ( выбрать репозитории и ветки, при их наличии.) Там же можно добавить пояснительный комментарий. Далее клацаем на кнопку и отправляем автору проекта. Там же есть возможность комментариев, где можно обсудить предлагаемые изменения.

### Branch или Ветки проекта
Ветки нужны, чтобы иметь возможность не работать с основной веткой `main`, а все манипуляции и модификации проводить с параллельной веткой. Это поможет избежать падение проекта при внесении новых изменений. Ветки мержаться только после их проверки и теста. Опять же, при возникновении конфликта всегда можно переключиться на другую, работоспособную ветку.
Так же, если над проектом работает несколько разработчиков, удобно когда они все работают по своим веткам.
Чтобы создать новую ветку в WS нужно зайти во вкладку Git и клацнуть на `+ New Brunch`. Называем её, чекаем `checkout branch`, тем самым переходя в новую ветку, и подтверждаем создание.
Чтобы объединить изменения новой ветки и основной ветки, нужно во вкладке Git WS перейти в ту ветку, в которую нужно добавить изменения из новой ветки( перейти в основную ветку). 
Далее, там же клацаем правой клавишей на новой ветке и выбираем пункт `merge 'ветка новая' into 'основная ветка'` . Коммитим и пушим.
Удалить созданную ветку за ненадобностью можно, во вкладке Git WS выбрать нужную ветку, клацнуть правой клавише и выбрать `delete` . Далее будет предложено удалить ветку с удалённого репозитория и локального. Выбираем, коммитим, пушим.

### Разрешение конфликтов в WS
При работе с разными ветками могут возникать конфликты при их объединении. IDE предупредит об этом, и если мы не знаем, что именно делать с конфликтом, то клацаем кнопку `Merge` и в ручную принимаем и удаляем конфликтный код.
![[Pasted image 20230219233850.png]]
![[Pasted image 20230219233914.png]]

### Git Stash / Unstash
Команда для создания временного хранилища незаконченного( незакомиченного кода). 
Позволяет выделить необходимый участок, клацнуть правой клавишей по нему, зайти во вкладку Git --> Stash Changes, в диалоговом окне дать название хранилищу, и создать его. При этом выделенный код исчезнет, и обратиться к нему позже можно будет при помощи команды  Git --> Uncommited chages --> Unstash Changes.
Там же появиться окно, в котором при нажатии на View, можно увидеть сравнение своего кода и кода Stash.
Stash вкладки можно удалять.
При таком положении - можно спокойно выполнять новую таску, не беспокоясь за оставленным незаконченным предыдущий код!
Время хранения - продолжительное!

### Локальная история Git
Локальная история поможет в случае, если забыли закоммитить код, закрыли WS и потеряли несохраненные данные. 
WS делает снимки с каждым изменением кода, и к ним можно обратиться, клацнув правой клавишей на любом участке кода, вызвать Locale History --> Show History. В диалоговом окне отобразятся изменения кода за последние 12 часов и ими можно будет манипулировать, в частности восстановить.

### Github Gist
Данная команда позволит сохранить на Github участок кода, компоненту - которую можно считать универсальной, и которую можно пере использовать в различных проектах. 
Такой код будет храниться на Github Gits, его можно сделать публичным, что другие разработчики могли его использовать, найдя его по поиску. Там же его можно корректировать, обсуждать, модифицировать.

#### Как создать Gits
Выделяем нужный участок кода, клацаем по нему правой клавишей, и выбираем команду `Create Gist`. В открывшемся диалоговом окне задаём описание данного гиста. Там же можно чекнуть настройку приватности гиста. Подтверждаем создание гиста.
Далее происходит перенаправление на Github Gist, где и будет храниться этот код. 
Попасть на Github Gist можно со своей страницы, нажав на опции профиля

#### Получение кода Gist через плагин для WS
Для установки плагина в WS дважды клацаем Shift. В диалоговом окне прописываем plugins. Откроется диспетчер плагинов, в поиске вбиваем нужный плагин. Выбираем и устанавливаем.
Для того, чтобы гисты работали, аккаунт github должен быть привязан к проекту

### Несколько учёток Github на одной машине
[stackov](https://stackoverflow.com/questions/3860112/multiple-github-accounts-on-the-same-computer/3860139#3860139) или [code.tutsplus](https://code.tutsplus.com/tutorials/quick-tip-how-to-work-with-github-and-multiple-accounts--net-22574)
Создаём новый профилm на Github, заходим в настройки профиля, клацаем `SSH and GPG keys`, далее на `Generating a new SSH key and adding it to the ssh-agent` Получаем строку
```shell
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```
Копируем её. С рабочего стола вызываем панел Git Bush, и вставляем эту строку, меняя `your_email@example.com` на email адреc нового аккаунта. Подтверждаем. Далее создаётся два ключа, приватный и публичный, в папке SSH на диске. Но! Если сейчас дать дальнейшее подтверждение в панели, то наш старый ключ просто пере-запишется, поэтому нужно его немного скорректировать. Идём в папку SSH и копируем путь к ней и вставляем его в панель за двоеточием
![[Pasted image 20230220204147.png]]
дописываем ключ вручную, с небольшим дополнением. Подтверждаем!

![[Pasted image 20230220204353.png]]
В папке SHH появятся новые ключи. Публичный ключ (расширение .pub) копируем и идём привязывать к своему новому аккаунту. Настройки --> SSH and GPG -->New SSH keys --> Вставляем и подтверждаем
Далее нужно в папке SSH создать и отредактировать файл config.
```shell
#Default GitHub
Host github.com
HostName github.com
 User git
 IdentityFile ~/.ssh/id_ed25519
 
#Dev2 GitHub account
Host github-safrondev2     //<-- меняем на путь к нашему аккаунту
HostName github.com 
 User git 
 IdentityFile ~/.ssh/id_ed25519_dev2   // <-- указываем новый ключ
```
Далее, при создании нового репозитория можно указывать новую ссылку `github-safrondev2` вместо `github.com` например.


#git
