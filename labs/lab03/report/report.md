---
## Front matter
title: "Отчёта по лабораторной работе №3"
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
babel-otherlangs: english
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

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.

# Задание

* Сделайть отчёт попредыдущей лабораторной работе в формате Markdown.
* В качестве отчёта предоставить отчёты в 3 форматах: pdf, docx и md (в архиве,
поскольку он должен содержать скриншоты, Makefile и т.д.)

# Выполнение лабораторной работы

1.	Добавляю картинки, чтобы затем их вставить в отчет.  

![Текст с описанием картинки](image/1.png)

![Текст с описанием картинки](image/2.png) 

2.	Указание цели работы. 

![Перенос из отчета цель работы](image/3.png)

3.	Указание задания. 

![Указание задания](image/4.png)

4.	Создание теоретического введения с командами, которые я использовала в лабораторной работе №2. 

![Теоретическое введение](image/5.png)

5.	Перенос текста из отчета с добавлением картинок и специальных вставок с кодом. 

![Перенос #1](image/6.png)

![Перенос #2](image/7.png)

6.	Сверка перенесенных данных. 

![Сверка](image/8.png)

7.	Указание вывода. 

![Вывод](image/9.png)

8.	Перенос контрольных вопросов со вставками кода. 

![Контрольные вопросы](image/10.png)

9.	Изменение заголовка и создателя файла. 

![Создатель файла](image/11.png)

10.	Комментирование изображений. 

![Комментирование изображений](image/12.png)


# Выводы

Изучила методы для создания и редактирования файлов формата Markdown. 
