# Инструкция по работе с Git

## Что такое Git?

***Git*** - это одна из реализаций распределенной системы контроля версий, поддерживающая локальные и удаленные репозитории. Самая популярная реализация Git - это [GitHub](https://www.github.com).

## Подготовка репозитория

Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущим репозиторием и там написать *git init*.

## Создание "сохранений"

### Добавление файла к коммиту

Для добавления файлу к коммиту используется команда *git add*. Для этого в терминале в папкой-репозиторием необходимо написать *git add <название файла>*.

### Выполнение коммита

Для того, чтобы выполнить коммит используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***

## Журнал изменений

Для просмотра истории коммитов используется команда *git log*. Для этого в терминале с папкой-репозиторием пишем *git log*. В журнале обязательно будут:
* хэш (номер) коммита
* дата и время коммита
* автор коммита
* текст сообщения к коммиту

## Перемещения между коммитами

Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <хэш коммита>*. Хэш коммита можно взять из истории коммитов, ро которую было рассказано в предыдущем пункте.

## Ветки в git

## Слияние веток и разрешение конфликтов

## Удаление веток

