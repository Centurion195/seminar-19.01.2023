# Инструкция по работе с Git

## Что такое Git?

***Git*** - это одна из реализаций распределенной системы контроля версий, поддерживающая локальные и удаленные репозитории. Самая популярная реализация Git - это [GitHub](https://www.github.com).

## Начало работы

После установки git необходимо «представиться» системе контроля версий. Это нужно сделать всего один раз, и git запомнит вас. Для этого нужно ввести в терминале 2 команды:

*git config --global user.name «Ваше имя английскими буквами»*

*git config --global user.email ваша*

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

Чтобы сравнить текущую версию и последнюю сохраненную необходимо воспользоваться командой *git diff*.

## Перемещения между коммитами

Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <хэш коммита>*. Хэш коммита можно взять из истории коммитов, ро которую было рассказано в предыдущем пункте.

## Ветки в git

Существует главная ветка *master* - чистовой, рабочий вариант работы/программы. Можно создавать ветки (черновики) для создания и тестрирования новых функций, изменений. После утверждения новых измений ветку-черновик можно слить в главную (master).

Для вывода списка всех существующих веток требуется ввести команду *git branch*. Символ (*) покажет, на какой ветке мы сейчас находимся.

### Создание веток

Чтобы создать ветку требуется выполнить команду: *git branch <название_ветки>*. При добавлении в команду флага "-b" сразу происходит переключение на новую ветку, например: *git checkout -b <название_ветки>*.

### Переключение между ветками

Чтобы переключиться на другую ветку требуется выполнить команду: *git checkout <название_ветки>*.

### Слияние веток и разрешение конфликтов

После завершения работы над своей задачей, рабочую ветку можно слить в master. Для этого нужно переключиться в ветку master и выполнить команду *merge*. Команда *merge* сливает указанную ветку в текущую! Например:

*git checkout master*

*git merge <название_ветки>*

При слиянии веток может случиться так, когда в одной и той же строки значатся новые изменения, тогда возникает конфликт, который требуется разрешить вручную. Вы увидите подобную картину:

```
<<<<< HEAD (current change)
...версия №1...
=====
...версия №2...
>>>>> lists (incoming change)
```

После разрешения конфликта обязательно требуется выполнить коммит.

### Удаление веток

Чтобы выполнить удаление ветки нужно выполнить команду: *git branch -d <название_ветки>*.