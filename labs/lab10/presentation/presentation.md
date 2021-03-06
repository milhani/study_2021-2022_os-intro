---
## Front matter
lang: ru-RU
title: Презентация лабораторной работы №10
author: |
	Ханина Людмила. Sevastianov\inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Презентация лабораторной работы №10

## Цель

Изучить основы программирования в оболочке ОС UNIX/Linux. Научиться писать небольшие командные файлы.

## Задание

* Написать скрипт, который при запуске будет делать резервную копию самого себя (то есть файла, в котором содержится его исходный код) в другую директорию backup в вашем домашнем каталоге. При этом файл должен архивироваться одним из архиваторов на выбор zip, bzip2 или tar. Способ использования команд архивации необходимо узнать, изучив справку.
* Написать пример командного файла, обрабатывающего любое произвольное число аргументов командной строки, в том числе превышающее десять. Например, скрипт может последовательно распечатывать значения всех переданных аргументов.
* Написать командный файл — аналог команды ls (без использования самой этой команды и команды dir). Требуется, чтобы он выдавал информацию о нужном каталоге и выводил информацию о возможностях доступа к файлам этого каталога.
* Написать командный файл, который получает в качестве аргумента командно йстроки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки.

# Выполнение лабораторной работы

## C помощью команды man узнаем информацию про zip, bzip2, tar

![zip](image/zip.png){ #fig:001 width=70% }

![bzip2](image/bzip2.png){ #fig:001 width=70% }

![tar](image/tar.png){ #fig:001 width=70% }

## Создаем файл lab01first.sh, в котором будем писать скрипт, который при запуске будет делать резервную копию самого себя в другую директорию backup в нашем домашнем каталоге. 

![Первый скрипт](image/1.1.png){ #fig:001 width=70% }

![Запускаем первый скрипт](image/1.2.png){ #fig:001 width=70% }

![Содержание архивированного файла](image/1.3.png){ #fig:001 width=70% }

## Далее создаем файл lab10second, в котором будет второй скрипт, обрабатывающий любое произвольное число аргументов командной строки, в том числе превышающее десять. Например, скрипт может последовательно распечатывать значения всех переданных аргументов

![Второй скрипт](image/2.1.png){ #fig:001 width=70% }

![Запускаем второй скрипт](image/2.2.png){ #fig:001 width=70% }

## Далее создаем файл lab10third, в котором будет третий скрипт, аналог команды ls (без использования самой этой команды и команды dir). Требуется, чтобы он выдавал информацию о нужном каталоге и выводил информацию о возможностях доступа к файлам этого каталога

![Третий скрипт](image/3.1.png){ #fig:001 width=70% }

![Запускаем третий скрипт](image/3.2.png){ #fig:001 width=70% }

## Далее создаем файл lab10fourth, в котором будет четвертый скрипт, который получает в качестве аргумента командной строки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки

![Четвертый скрипт](image/4.1.png){ #fig:001 width=70% }

![Запускаем четвертый скрипт](image/4.2.png){ #fig:001 width=70% }

# Выводы

Я научилась писать небольшие командный файлы для решения различных вопрсов
