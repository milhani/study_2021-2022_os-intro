---
## Front matter
title: "Лабораторная работа №4"
author: "Ханина Людмила Константиновна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.

# Задание

1. Определите полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
2. Выполните следующие действия:
2.1. Перейдите в каталог /tmp.
2.2. Выведите на экран содержимое каталога /tmp. Для этого используйте команду ls с различными опциями. Поясните разницу в выводимой на экран информации.
2.3. Определите,есть ли в каталоге /var/spool подкаталог с именем cron?
2.4. Перейдите в Ваш домашний каталог и выведите на экран его содержимое. Определите, кто является владельцем файлов и подкаталогов?
3. Выполните следующие действия:
3.1. В домашнем каталоге создайте новый каталог с именем newdir.
3.2. В каталоге ~/newdir создайте новый каталог с именем morefun.
3.3. В домашнем каталоге создайте одной командой три новых каталога с именами letters, memos, misk. Затем удалите эти каталоги одной командой.
3.4. Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверьте, был ли каталог удалён.
3.5. Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте, был ли каталог удалён.
4. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов, входящих в него.
5. С помощью команды man определите набор опций команды ls,позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием файлов.
6. Используйте команду man для просмотра описания следующих команд: cd, pwd, mkdir, rmdir, rm. Поясните основные опции этих команд.
7. Используя информацию, полученную припомощи команды history,выполните модификацию и исполнение нескольких команд из буфера команд.

# Теоретическое введение

| Команда | Значение команды                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `pwd`          | Узнать абсолютный путь каталога/файла, в котором находишься      |
| `ls`      |   Узнать содержимое каталога   |
| `ls -a`       | Узнать содержимое каталога в том числе и скрытые файлы/каталоги     |
| `ls -l`      | Узнать содержимое каталога и информацию о нем (владелец, доступ и прочее) |
| `cd dir`     | Перейти в каталог dir   |
| `mkdir dir`      | Создать каталог dir    |
| `mrdir dir`       | Удалить пустой каталог dir       |
| `rm -r dir`       | Удалить каталог dir         |

# Выполнение лабораторной работы

1. Запускаем виртуальную машину. В ней открываем терминал.

![Виртуальная машина](image/1.png){ #fig:001 width=70% }

![Терминал](image/2.png){ #fig:001 width=70% }

2. Чтобы определить полное имя домашнего каталога воспользуемся командой pwd. 

![Полное имя домашнего каталога](image/3.png){ #fig:001 width=70% }

3. С помощью команды cd /tmp переходим в каталог tmp. Далее выводим его содержимое различными способами. Способ первый — ls. 

![ls](image/ls.png){ #fig:001 width=70% }

Способ второй
```
ls -a
```
Тогда мы увидим еще и скрытые файлы и каталоги. 

![ls -a](image/ls -a.png){ #fig:001 width=70% }

Способ третий
```
ls -alF
```
Тогда мы увидим информацию о каталогах и файлах, включая скрытные. 

![ls -alF](image/ls -alF.png){ #fig:001 width=70% }

# Выводы

Здесь кратко описываются итоги проделанной работы.

