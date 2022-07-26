 
![logo](https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png "Логотип GIT")

## Инструкция для работы с Git и удалёнными репозиториями

---

*Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.*

[GUI Clients](https://git-scm.com/downloads/guis) - ссылка на клиенты GUI.

*Теперь, когда Git установлен в вашей системе, самое время настроить среду для работы с Git под себя. Это нужно сделать только один раз — при обновлении версии Git настройки сохранятся. Но, при необходимости, вы можете поменять их в любой момент, выполнив те же команды снова.*

*Первое, что вам следует сделать после установки Git — указать ваше имя и адрес электронной почты.*

>$ git config --global user.name "John Doe"

>$ git config --global user.email johndoe@example.com

# Подготовка репозитория
![startrep](https://git-scm.com/book/en/v2/images/centralized_workflow.png "Подготовка репозитория")

## git init
>Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git) Инициализация: указываем папку, в которой git начнёт отслеживать изменения. В папке создаётся скрытая папка .git.

## git add
>Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

## git status
>Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

# Создание коммитов
![commitcreate](https://git-scm.com/book/en/v2/images/head-to-master.png "Создание коммитов")

## git commit
>Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## git checkout
>Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## git log
>Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

# Ветки в Git
![vetki](https://git-scm.com/book/en/v2/images/branch-and-history.png "Ветки в GIT")

## git branch
>Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

## git merge
>Для того чтобы дабавить ветку в текущую ветку используется команда *git merge <name branch>*

## git branch -d
>Для удаления ветки ввести команду "git branch -d 'name branch'"

# Конфликт изменений
![konflikt](https://git-scm.com/book/en/v2/images/undomerge-reset.png "Конфликт изменений")

>При работе в двух ветках одновременно может возникнуть ситуация, когда в одной и другой ветке мы по-разному изменили блок текста. Если затем мы попробуем слить эти ветки, Git сообщит о конфликте и предложит выбрать, какие же изменения записать.

# Работа с удаленными репозиториями. Скачивание из текущего репозитория и слияние со своей версией

![github](https://miro.medium.com/max/1200/1*mtsk3fQ_BRemFidhkel3dA.png "Работа с удаленными репозиториями")

## git clone
>Команда git clone составная: она не только загружает все изменения, но и пытается слить все ветки на локальном компьютере и в удаленном репозитории.

## git pull
>Эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией.

## git push
>Отправить свою версию репозитория во внешний репозиторий поможет команда git push. При первом её использовании нужна git pull авторизация. 

*Эта команда позволяет отправить нашу версию репозитория на внешний репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ на внешнем репозитории.*

## Как настроить совместную работу. Углубляемся в контроль версий 
1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории.
4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно, 
вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория

## pull request
>➜ команда для предложения изменений

>➜ запрос на вливание изменений в репозиторий

>В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают команду pull request. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет изменения командой push в свой аккаунт на GitHub и даёт команду pull request. 