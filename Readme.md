# Инструкция по работе с Git

## Что такое Git?

***Git*** - это одна из реализаций распределенной системы контроля версий, поддерживающая локальные и удаленные репозитории. Самая популярная реализация Git - это [GitHub](https://www.github.com).

## Начало работы

<<<<<<< HEAD
-  status
- .gitignor
=======
После установки git необходимо «представиться» системе контроля версий. Это нужно сделать всего один раз, и git запомнит вас. Для этого нужно ввести в терминале 2 команды:

*git config --global user.name «Ваше имя английскими буквами»*

*git config --global user.email ваша*
>>>>>>> Start

## Подготовка репозитория

Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и там написать *git init*.

### Статус файлов в репозитории

Для просмотра статуса файлов, а именно: все ли файлы отслеживаются git, есть ли незафиксированные изменененные отслеживаемые файлы, есть ли добавленные, но не "закоммиченные" файлы используется команда *git status*.

Чтобы git начал игнорировать некоторые файлы и не сообщал о них в статусе требуется создать файл в корне репозитория с именем ".gitignor", в котором в каждой строчке нужно прописать имена файлов с расширением, которые требуется не учитывать. После этого добавить и зафиксировать данный файл.

*git add .gitignor*

*git commit -m "File gitignore added"*

## Создание "сохранений"

### Добавление файла к коммиту

Для добавления файлу к коммиту используется команда *git add*. Для этого в терминале в папкой-репозиторием необходимо написать *git add <название файла>*. Чтобы добавить все файлы в репозитории необхрдимо написать *git add --all*.

### Выполнение коммита

Для того, чтобы выполнить коммит используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***

## Журнал изменений

Для просмотра истории коммитов используется команда *git log*. Для этого в терминале с папкой-репозиторием пишем *git log*. В журнале обязательно будут:
* хэш (номер) коммита
* дата и время коммита
* автор коммита
* текст сообщения к коммиту

Для графического вывода веток необходимо воспользоваться командой *git log --graph*.

## Сравнение версий



## Перемещения между коммитами

Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <хэш коммита>*. Хэш коммита можно взять из истории коммитов, ро которую было рассказано в предыдущем пункте.

## Ветки в git

### Создание веток

### Переключение между ветками

### Слияние веток и разрешение конфликтов

### Удаление веток

