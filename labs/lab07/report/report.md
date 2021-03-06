---
## Front matter
title: "Лабораторная работа №7"
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

Освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.

# Задание

* Задания по mc
* Задания по встроенному редактору mc

# Теоретическое введение

| Команда | Значение команды                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `mc`          | Запуск командной оболочки Midnight Commander     |
| `man command`       | Узнать информацию о команде command     |


# Выполнение лабораторной работы

1. С помощью команды mac mc изучаем информацию о командной оболочке. Далее запускаем ее. 

2. Поработаем с панелями. Например, скопируем файл и посмотрем права доступа. 

![Права доступа](image/1.3.1.png){ #fig:001 width=70% }

![Копирование](image/1.3.2.png){ #fig:001 width=70% }

3. Изучим команды левой (и правой) панели. Изменим формат вывода информации о файлах. 

![Команды левой (и правой) панели](image/1.4.1.png){ #fig:001 width=70% }

![Формат вывода информации о файлах](image/1.4.2.png){ #fig:001 width=70% }

4. Используем возможности подменю Файл. Посмотрим содержимое файла. (Перед этим его создаем.) Далее выбираем редактирование содержимого текстового файла.

![Команды подменю Файл](image/1.5.1.png){ #fig:001 width=70% }

![Просматриваем файл](image/1.5.2.png){ #fig:001 width=70% }

![Редактируем](image/1.5.3.png){ #fig:001 width=70% }

5. Далее создаем каталог и копируем наш файл в этот каталог. 

![Создаем каталог](image/1.5.4.png){ #fig:001 width=70% }

![Копируем файл в каталог](image/1.5.5.png){ #fig:001 width=70% }

6. Используем возможности подменю Команда. 

![Команды подменю Команда](image/1.6.0.png){ #fig:001 width=70% }

Поищем в файловой системе файлы, которые содержат слово file. 

![Поиск в файловой системе файла с заданными условиями](image/1.6.1.png){ #fig:001 width=70% }

Далее посмотрим историю использованных команд. Повторим одну из них. Затем перейдем в домашних каталог. 

![Просматриваем историю использованных команд](image/1.6.2.png){ #fig:001 width=70% }

![Переход в домашний каталог](image/1.6.3.png){ #fig:001 width=70% }

Проанализируем файл меню и файл расширений.

![Редактирование файла меню](image/1.6.4.png){ #fig:001 width=70% }

![Файл меню](image/1.6.5.png){ #fig:001 width=70% }

7. Рассмотрим возможности подменю Настройки. Например, изменим цветовое оформление. 

![Возможности подменю Настройки](image/1.7.1.png){ #fig:001 width=70% }

![Измение цветового оформления](image/1.7.2.png){ #fig:001 width=70% }

8. Теперь поработаем со внутренним редактором mc. Создадим текстовый файл и откроем его с помощью встроенного в mc редактора.

![Создаем файл](image/2.1.png){ #fig:001 width=70% }

![Открываем его в редакторе mc](image/2.2.png){ #fig:001 width=70% }

Далее находим в интернете любой текст и вставляем его в файл. 

![Вставляем текст в файл](image/2.3.png){ #fig:001 width=70% }

9. Начинаем работать с этим файлом. Удаляем строку с помощью горячих клавиш Ctrl-y. 

![Была строка](image/2.4.1.1.png){ #fig:001 width=70% }

![Нет строки](image/2.4.1.2.png){ #fig:001 width=70% }

Далее выделяем часть текста с помощью клавиши F3 и копируем его с помощью клавиши F5. 

![Выделили часть текста](image/2.4.2.1.png){ #fig:001 width=70% }

![Скопировали часть текста](image/2.4.2.2.png){ #fig:001 width=70% }

Затем выделяем часть текста с помощью клавиши F3 и переносим ее на новую строку с помощью клавиши F6. Сохраняем файл. С помощью клавиш Ctrl-u отменяем последнее действие. 

![Выделили часть текста, перенесли и сохранили файл](image/2.4.3-2.4.4.png){ #fig:001 width=70% }

Далее переходим в конец файла с помощью сочетаний Ctrl-End и пишем фразу 'the last string'. Аналогичего переходим в начало файла только уже с помощью команды Ctrl-Home и пишем фразу 'the first string'. Сохраняем и закрываем файл. 

![Переходим в конец/начало файла и записываем строку](image/2.4.6-2.4.7.png){ #fig:001 width=70% }

10. Я специально создала файл text.py, в котором содержится код на Python. Открываем его.

![Открываем код](image/2.5.png){ #fig:001 width=70% }

Нажимаем F9, в подменю Команды включаем подсветку синтаксиса. 

![Подсветка синтаксиса](image/2.6.png){ #fig:001 width=70% }

# Контрольные вопросы

1. Режимы работы в mc:
 • Информация: на панель выводятся сведения о файле и текущей файловой системе,
расположенных на активной панели;
 • Дерево: на одной из панелей выводится структура дерева каталогов.   

2. С помощью комбинаций клавиш в mc можно просмотреть содержимое файла (F3), изменить содержимое файла (F4), скопировать файлы (F5), перенести файлы (F6), создать подкаталог (F7), удалить файл/каталог (F8). 

3. Струтура левой (и правой) панели:
 • Формат списка позволяет управлять отображением файлов и каталогов. 
 • Порядок сортировки позволяет задать критерий сортировки при выводе списка файлов. 

4. Структура Файл:
 • Просмотр (F3) позволяет просматривать файл. 
 • Правка (F4) позволяет изменять файл. 
 • Копирование (F5) позволяет копировать указанный файл/каталог в определенное место
 • Права доступа позволяют указать или изменить права доступа к файлам/каталогам. 
 • Создание каталога (F7) позволяет создать каталог. 
 • Удалить (F8) позволяет удалить файл/каталог. 

5. Структура Команда:
 • Дерево каталогов — отображает структуру каталогов. 
 • Поиск файлов — выполняет поиск файлов по заданным параметрам. 
 • Сравнить каталоги — сравнивает содержимое каталогов. 
 • История командной строки – выводит историю использованных команд. 

6. Структура Настройки:
 • Конфигурация — позволяет скорректировать настройки работы с панеляи. 
 • Внешний вид и Настройки панелей — изменяет расположение панелей и их цветовыделение. 

7. Встроенные команды mс:
 • F1 — Помощь
 • F2 — Сохранить изменения в файл при редактировании
 • F3 — Просмотр файла
 • F3 — (Во время редактирования) Начать выделение текста. Повторное нажатие F3 закончит выделение
 • F4 — Редактирование файла
 • F5 — Скопировать выделенное
 • F6 — Переместить выделенное
 • F8 — Удалить выделенное  

8. Команды встроенного редактора mc:
 • F4 — поиск с заменой
 • F6 — поиск с помощью регулярного выражения
 • Shift+F3 — Начать выделение блока текста. Повторное нажатие F3 закончит выделение
 • Shift+F5 — Вставка текста из внутреннего буфера обмена mc (прочитать внешний файл)
 • Ctrl+f — Занести выделенный фрагмент во внутренний буфер обмена mc (записать во внешний файл)
 • Ctrl+k — Удалить часть строки до конца строки
 • Ctrl+s — Включить или выключить подсветку синтаксиса
 • Ctrl+u — Отменить действия
 • Ctrl+y — Удалить строку


9. Файлы меню содержат списки команд для выполнения часто повторяемых пользователем операций. Эти меню создаются и поддерживаются самими пользователями. Могут быть созданы три файла меню: в текущем каталоге, в домашнем каталоге пользователя и общесистемный.

10. Операции над файлами:
 • Shift+F4 — Создает новый файл
 • shift-f6 — переименовать файл
 • alt-. — показать скрытые файлы
 • ctrl-x, c — права на файл
 • ctrl-x, o — владелец файла
 • Shift-F3 — просмотр файла
 • Ctrl-X+L — создать ссылку на файл
 • Ctrl-X+S — создать символическую ссылку на файл
 • F12 — Save as
 • ctrl-x, ctrl-d — сравнить файлы

# Выводы

Я научилась работать в mc. Узнала его режими и возможности. Научилась редактировать файлы с помощью встроенного в mc редактора. 
