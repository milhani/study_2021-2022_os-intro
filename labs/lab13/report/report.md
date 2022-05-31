---
## Front matter
title: "Лабораторная работа №13"
author: "Ханина Людмила Константиновна"

## Generic otions
lang: ru-RU

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

Приобрести простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.
# Задание

* В домашнем каталоге создайте подкаталог ~/work/os/lab_prog.
* Создайте в нём файлы:calculate.h, calculate.c, main.c.
* С помощью gdb выполните отладку программы calcul. 
* С помощью утилиты splint попробуйте проанализировать коды файлов calculate.c и main.c.

# Выполнение лабораторной работы

1. В домашнем каталоге создаем подкаталог ~/work/os/lab_prog.

![Создаем подкаталог ~/work/os/lab_prog](image/1.png){ #fig:001 width=70% }

2. Создаем в нём файлы: calculate.h, calculate.c, main.c.
Это будет примитивнейший калькулятор, способный складывать, вычитать, умножать и делить, возводить число в степень, брать квадратный корень, вычислять sin, cos, tan. При запуске он будет запрашивать первое число, операцию, второе число. После этого программа выведет результат и остановится. 

![calculate.c](image/2.1.png){ #fig:001 width=70% }

![calculate.h](image/2.2.png){ #fig:001 width=70% }

![main.c](image/2.3.png){ #fig:001 width=70% }

3. Выполняем компиляцию программы посредством gcc. Синтаксических ошибок нет.

![Компиляцию программы посредством gcc](image/3.png){ #fig:001 width=70% }

4. Создаем Makefile. Этот файл нужен для автоматической компиляции файлов и объединения их в один исполняемый файд calcul. clean удаляет все файлы. Переменная CC отвечает за утилиту компиляции; CFLAFS — опции данной утилиты; LIBS — опции для объединения объектных файлов в один исполняемый файл. 

![Makefile](image/5.png){ #fig:001 width=70% }

5. Исправляем Makefile и выполняем компиляцию файлов. 

![Испрвляем Makefile](image/6.1.png){ #fig:001 width=70% }

![Выполняем компиляцию файлов](image/6.2.png){ #fig:001 width=70% }

6. Запускаем отладчик GDB. 

![Запускаем отладчик GDB](image/6.3.png){ #fig:001 width=70% }

7. Запускаем программу с помощью команды run.

![Запускаем программу](image/6.4.png){ #fig:001 width=70% }

8. Для постраничного просмотра исходного кода используем команду list. Для просмотра строк с 12 по 15 используем команды list 12,15. А чтобы посмотреть определенные строки неосновного файла, то нужно использовать list с параметрами. Например, list calculate.c:20,29. 

![Просмотр строк](image/6.5.png){ #fig:001 width=70% }

9. Устанавливаем точку останова в файле calculate.c на строке номер 21 и выводим информацию обо всех имеющихся точках останова. 

![Устанавливаем точку остановки](image/6.6.png){ #fig:001 width=70% }

10. Запускаем программу и убеждаемся, что она остановится в момент прохождения breakpoint'a. 

![Остановка программы](image/6.7.png){ #fig:001 width=70% }

11. Посмотрим значение переменной Numeral и сравним его с результатом вывода команды display Numeral. 

![Numeral](image/6.8.png){ #fig:001 width=70% }

12. Уберем точки останова. 

![Уберем точки остановки](image/6.9.png){ #fig:001 width=70% }

13. С помощью утилиты splint узнаем, что в файле calculate.c просходит сравнение вещесвтенного числа с нулем, а в main.c есть функция scanf, которая возращает целое число, которое нигде не используется.  

![splint calculate.c](image/7.1.png){ #fig:001 width=70% }

![splint main.c](image/7.2.png){ #fig:001 width=70% }

# Контрольные вопросы

1. while [$1 != "exit"]

В данной строчке допущены следующие ошибки:

* не хватает пробелов после первой скобки и перед второй скобкой;
* выражение $1 необходимо взять в "".

Таким образом, правильный вариант должен выглядеть так: while [ "$1" != "exit" ]

2. Для объединения строк в одну можно воспользоваться следующими способами:
* newstring="$s1$s2"
* string += "text"

3. Утилита seq выводит последовательность целых чисел с шагом, заданным пользователем.
*  Чтобы просто напечатать последовательность чисел, начиная с 1 и заканчивая n, используйте следующую команду: seq n;
*  Можно указать верхний и нижний пределы: seq begin end (seq 1 3 -> 1 2 3);
*  Также можно указать шаг: seq begin step end (seq 1 3 10 -> 1 4 7 10). 

4. Ответом будет 3, так как было использовано целочисленное деление. 

5. Основные ключевые различия между Zsh и Bash:
* Zsh более интерактивный и настраиваемый, чем Bash.
* У Zsh есть поддержка с плавающей точкой, которой нет у Bash.
* В Zsh поддерживаются структуры хеш-данных, которых нет в Bash.
* Функции вызова в Bash лучше по сравнению с Zsh.
* Внешний вид подсказки можно контролировать в Bash, тогда как Zsh настраивается.
* Конфигурационными файлами являются .bashrc в интерактивных оболочках без регистрации и .profile или .bash_profile в оболочках входа в Bash. В Zsh оболочками, не входящими в систему, являются .zshrc, а оболочками для входа - .zprofile.
* Массивы Zsh индексируются от 1 до длины, тогда как Bash индексируется от -1 до длины.
* В Zsh, если шаблоны не совпадают ни с одним файлом, выдается ошибка. Находясь в Баше, он остается без изменений.

6. Синтаксис верен. 

7. Преимущества sh:
* стандартизировано;
* это намного проще и легче узнать;
* он переносится через системы POSIX - даже если они не имеют bash, они должны иметь sh.

Есть и преимущества использования bash. Его функции делают программирование более удобным и похожим на программирование на других современных языках программирования. К ним относятся такие области, как локальные переменные и массивы. Обычный sh - очень минималистический язык программирования.

# Выводы

Я научилась запускать откладчик GDB, работать с ним и тестировать программы. 
