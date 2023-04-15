# Что такое Git и зачем он нужен?

**_Git_** - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. 

# Настройка

Открываем терминал (Linux и MacOS) или консоль (Windows) и вводим следующие команды.

Установим имя для вашего пользователя
Вместо <ваше_имя> можно ввести, например, **Grisha_Popov**
Кавычки оставляем
**git config --global user.name "<ваше_имя>"**
Теперь установим email. Принцип тот же.
**git config --global user.email "<адрес_почты@email.com>"**

# Команды, используемые для работы с репозиторием

* **git init** инициализируем репозиторий

* **git status** - общий статус гита

* **git add <file_name>** добавить версионность файла

* **git add .** - добавить всем файлам версионность

* **git commit** фиксирование изменений

* **git commit -m"message"** фиксирование изменений напрямую в терменале

* **git commit -am "message"** фиксирование изменений в терменале напрямую без использования git add

* **git log** глянуть историю commit

* **git checkout master** вернутся в обычное состояние

* **(terminal powershell) new-item file.name** - создание нового файла

# Процесс работы с Git
Не стоит после каждого изменения файла делать commit. Чаще всего их создают, когда:

* Создан новый функционал
* Добавлен новый блок на верстке
* Исправлены ошибки по коду
* Вы завершили рабочий день и хотите сохранить код

Это поможет держать вашу ветки в чистоте и порядке. Тем самым, вы будете видеть историю изменений по каждому нововведению в вашем проекте, а не по каждому файлу.

# Совместная работа (дополняем информацией с семинара 2)
Для этого вам пригодится ветвление

***Ветка*** - это набор *commit* (кружок), которые идут друг за другом. У ветки есть название, основную ветку чаще всего называют master (на картинках будет называться main) . Если говорить простыми словами, то ветка master - это наш проект.

Другие ветки - это отдельное место для реализации нового функционала или исправление багов (ошибок) нашего проекта. То есть, с отдельной веткой вы делаете что угодно, а затем сливаете эти изменения в основную ветку master.

Для того, чтобы создать новую ветку вводим:

***git branch*** <название_ветки>

или вот так

***git checkout -b*** <название_ветки>
создать новую ветку и сразу же в нее переместиться.

**git merge branch_name** - соединить изменения из branch_name, с веткой, в которой мы находимся.

**git checkout branch_name** - перемещение на ветку branch_name

> Ветка master в Git ничем не отличается от остальных. Но она присутствует практически в каждом репозитории, потому что создается командой *git init* по умолчанию, 
а большинство пользователей не утруждают себя переименованием.
(C.Чакон, Б. Штрауб "Git для профессионального программиста")

[Для облегчения обучения, ссылка на бесплатный тренажер по Git](https://learngitbranching.js.org/)

[Справочные материалы по Markdown](https://learn.microsoft.com/ru-ru/contribute/markdown-reference)