# инструкция
## ***Оглавление***

* Основные команды 

* Работа с тектом 

* Работа с ветками

* информация о работе с удаленными репозиториями

### Основные команды
```
 1. git init - создать новый проект в текущей директории
 2. git status - показать состояние репозитория
 3. git add - добавить в индекс все новую версию
 4. git commit -m "Name of commit" -  зафиксировать в коммите проиндексированные изменения
 5. git log master - показать коммиты
 6. git branch - показать список веток
 7. git merge name - влить в ветку, в которой находимся
 8. git checkout master - переключаемся на ветку master
 9. git push - отправляем коммит с быстрым критическим изменением в master в удалённом репозитории
 ```
 
 ### Работа с тектом в GIT
```
# Это заголовок с тегом <h1>
## Это заголовок с тегом <h2>
###### Это заголовок с тегом <h6>
```
```
**Этот текст будет выделен жирным**
__Этот текст также будет выделен жирным__
```
немножко эмодзи
```
:+1: :camel: :cactus: :rocket: :unicorn: 
```
немного задач
```
- [x] выполненная задача
- [ ] не выполненная задача
```
### Работа с ветками

```
git branch                    # показать список веток
git branch -v                 # показать список веток и последний коммит в каждой
git branch new_branch         # создать новую ветку с указанным именем на текущем коммите
git branch new_branch name    # создать новую ветку с указанным именем на указанном коммите
git branch -f master name     # переместить ветку master на указанный коммит
git branch -f master master~2 # переместить ветку master на 2 коммита назад
git checkout new_branch       # перейти в указанную ветку
git checkout -b new_branch    # создать новую ветку с указанным именем и перейти в неё
git checkout -B master NAME   # переместить ветку с указанным именем на указанный коммит и перейти в неё
git merge hotfix              # влить в ветку, в которой находимся, данные из ветки hotfix
git merge hotfix -m "Горячая правка" # влить в ветку, в которой находимся, данные из ветки hotfix (указано сообщение коммита слияния)
git merge hotfix --log        # влить в ветку, в которой находимся, данные из ветки hotfix, показать редактор описания коммита, добавить в него сообщения вливаемых коммитов
git merge hotfix --no-ff      # влить в ветку, в которой находимся, данные из ветки hotfix, запретить простой сдвиг указателя, изменения из hotfix «останутся» в ней, а в активной ветке появится только коммит слияния
git branch -d hotfix          # удалить ветку hotfix (используется, если её изменения уже влиты в главную ветку)
git branch --merged           # показать ветки, уже слитые с активной
git branch --no-merged        # показать ветки, не слитые с активной
git branch -a                 # показать все имеющиеся ветки (в т.ч. на удаленных репозиториях)
git branch -m old_branch_name new_branch_name # переименовать локально ветку old_branch_name в new_branch_name
git branch -m new_branch_name # переименовать локально ТЕКУЩУЮ ветку в new_branch_name
git push origin :old_branch_name new_branch_name # применить переименование в удаленном репозитории
git branch --unset-upstream   # завершить процесс переименования
```


 информация о работе с удаленными репозиториями

 ```
 git remote -v              # показать список удалённых репозиториев, связанных с локальным
git branch -r              # показать удаленные ветки
git branch -a              # показать все ветки(локальные и удаленные)       
git remote remove origin   # убрать привязку удалённого репозитория с сокр. именем origin
git remote add origin https://github.com:nicothin/test.git # добавить удалённый репозиторий (с сокр. именем origin) с указанным URL
git remote rm origin       # удалить привязку удалённого репозитория
git remote show origin     # получить данные об удалённом репозитории с сокращенным именем origin
git fetch origin           # скачать все ветки с удаленного репозитория (с сокр. именем origin), но не сливать со своими ветками
git fetch origin master    # то же, но скачивается только указанная ветка
git checkout --track origin/github_branch # создать локальную ветку github_branch (данные взять из удалённого репозитория с сокр. именем origin, ветка github_branch) и переключиться на неё
git push origin master     # отправить в удалённый репозиторий (с сокр. именем origin) данные своей ветки master
git pull origin            # влить изменения с удалённого репозитория (все ветки)
git pull origin master     # влить изменения с удалённого репозитория (только указанная ветка)
 ```
 