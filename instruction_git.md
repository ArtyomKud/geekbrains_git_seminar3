# **Инструкция по работе с GIT**

![git emblem](git.JPG)

## Предварительная настройка с GIT

Чтобы "представиться" программе GIT нужно ввести команды:

    git config --global user.name "Ваше имя" 
    git config --global user.email "Ваш е-маил"

## Создание репозитория

Чтобы инициализировать новый репозиторий нужно ввести команду:

    git init

## Добавление в индекс

Чтобы добавить изменения в индекс (для фиксации в следующим коммите) нужно ввести команду:

    git add <имя файла>

## Фиксация изменений

Чтобы зафиксировать изменения, добавленные в индекс нужно ввести команду:

    git commit

## Фиксация изменений с использованием опции <-m>

Чтобы при фиксации изменений оставить сообщение о коммите с вводом сообщения тут же в терминале нужно ввести команду следующим образом:

    git commit -m "Ваше сообщение"

## Фиксация изменений с использованием опции <-a>

Чтобы зафиксировать все изменения в отслеживаемых файлах введите команду следующим образом:

    git commit -a

## Фиксация изменений с использованием опций <-am>

Чтобы совместить команды git add и git commit -m
введите команду следующим образом:

    git commit -am

## Просмотр истории коммитов

Чтобы просмотреть историю коммитов нужно ввести команду:

    git log

## Просмотр истории коммитов в компактном виде

Чтобы просмотреть историю коммитов в коипактном виде нужно ввести команду:

    git log --oneline

## Просмотр истории коммитов c использованием опции --all

Обычная команда git log показывает историю коммитов начиная с последнего коммита или коммита на который было перемещения и в таком случае для просмотра полной стории коммитов необходимо ввести команду:

    git log --all

## Просмотр истории коммитов с опциями --all --oneline

Для промотра полной истории коммитов в компактном режиме введите команду:

    git log --all --oneline

## Сравнение текущего файла с репозиторием

Для сравнения текущего файла с версией в репозитории введите команду:

    git diff

## Сравнение двух коммитов между собой

Для сравнения двух коммитов между собой введите команду:

    git diff hash1 hash2

где hash1 и hash2 первые 7 цифр идентификаторов коммитов

## Переход на определенный коммит

Для перехода на определенный коммит введите команду:

    git checkout hash

где hash первые 7 цифр идентификатора коммита

## Просмотр изменений  текущем репозитории

Для просмотра изменений в текущем репозитории введите команду:

    git status

## Переход на последний коммит ветки

Для перехода на последний коммит определенной ветки введите команду:

    git checkout master

где master название ветки

## Ветвления

Ветвления в git нужны, чтобы несколько программистов могли вести работу над одним и тем же проектом или даже файлом одновременно, при этом не мешая друг другу.
Кроме того, ветки используются для тестирования экспериментальных функций: чтобы не повредить основному проекту, создается новая ветка специально для экспериментов. Если эксперимент удался, изменения с экспериментальной ветки переносятся на основную, если нет – новая ветка попросту удаляется, а проект остается нетронутым.
Помимо прочего, ветки можно использовать для разных выходящих параллельно релизов одного проекта. Например, в репозитории Python может быть две ветки: python-2 и python-3. До закрытия python-2 релизы этих версий языка выходили независимо друг от друга, поэтому могло иметь место такое разделение на ветки.

## Создание новой ветки

Для создания новой ветки введите команду:

    git branch name_branch

где name_branch - имяновой ветки.

## Слияние веток

Для слияния веток введите следующую команду:

    git merge name_branch

где name_branch - имя вливаемой ветви
при сливании нужно находиться в ветви, в которую планируется вливать.
При возникновении конфликта нужно:
- для IDE выбрать: 
   
    - принять текущие изменения
    - принять входящие изменения
    - принять и те и другие изменения
    - сравнить
- сам GIT сохранит и текущие и входящие изменения, поэтому нужно вручную скорректировать текст.
После разрешения конфликта нужно сохранить изменения и закоммитить 

     git commit -m "merge commit: merge name_branch"



## Удаление ветки

Для удаления ветки введите команду:

    git branch -d name_branch

где name_branch - имя удаляемой ветки
флаг -d позволит удалить только влитую ветку,
для принудительного удаления используйте флаг -D

## Удаленные репозитории

Удаленные репозитории нужны для того чтобы ...
