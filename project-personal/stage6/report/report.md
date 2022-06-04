---
## Front matter
title: "Отчёт по ИП этап 6"
author: "Ханина Людмила Константиновна"

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

# Задание

* Сделать поддержку английского и русского языков.
* Разместить элементы сайта на обоих языках.
* Разместить контент на обоих языках.
* Сделать пост по прошедшей неделе.
* Добавить пост на тему по выбору (на двух языках). 

# Выполнение лабораторной работы

1. Запускаю ~/bin/hugo server и начинаю работать с сайтом. 

2.  Захожу в файл macblog/config/_default/languages.yaml. Добавляю туда русский язык. 

![macblog/config/_default/languages.yaml](image/lang.png){ #fig:001 width=70% }

3. Меняю файл menus.yaml на файлы menus.ru.yaml и menus.en.yaml. Меняем названия разделов на русском. 

![Файлы](image/menuses.png){ #fig:001 width=70% }

![menus.ru.yaml](image/menus.ru.png){ #fig:001 width=70% }

4. Далее идем в папку content и создаем там две папки ru и en, где будут лежать все необходимые папки с материалами на русском и английском языках соответственно.  

![content](image/content.png){ #fig:001 width=70% }

5. Начинаем переводить данные на русский. Достижения:

![Достижения](image/accom1.png){ #fig:001 width=70% }

![Достижения](image/accom2.png){ #fig:001 width=70% }

6. Контакты:

![Контакты](image/contact1.png){ #fig:001 width=70% }

![Контакты](image/contact2.png){ #fig:001 width=70% }

7. События:

![События](image/event1.png){ #fig:001 width=70% }

![События](image/event2.png){ #fig:001 width=70% }

8. Опыт:

![Опыт](image/exper1.png){ #fig:001 width=70% }

![Опыт](image/exper2.png){ #fig:001 width=70% }

9. Избранные публикации:

![Избранные публикации](image/featured1.png){ #fig:001 width=70% }

![Избранные публикации](image/featured2.png){ #fig:001 width=70% }

10. Посты:

![Посты](image/post1.png){ #fig:001 width=70% }

![Посты](image/post2.png){ #fig:001 width=70% }

11. Проекты:

![Проекты](image/proj1.png){ #fig:001 width=70% }

![Проекты](image/proj2.png){ #fig:001 width=70% }

12. Публикации:

![Публикации](image/publish1.png){ #fig:001 width=70% }

![Публикации](image/publish2.png){ #fig:001 width=70% }

13. Навыки:

![Навыки](image/skills1.png){ #fig:001 width=70% }

![Навыки](image/skills2.png){ #fig:001 width=70% }

14. Теперь переведем некоторые разделы на английский. Биография:

![Биография](image.en/bio.png){ #fig:001 width=70% }

15. Контакты:

![Контакты](image.en/contact.png){ #fig:001 width=70% }

16. Публикации:

![Публикации](image.en/public.png){ #fig:001 width=70% }

17. Достижения и посты:

![Достижения и посты](image.en/accomppost.png){ #fig:001 width=70% }

18. Проекты и события:

![Проекты и события](image.en/projevent.png){ #fig:001 width=70% }

19. Навыки и опыт: 

![Навыки и опыт](image.en/skillandexp.png){ #fig:001 width=70% }

20. Далее создадим пост про прошедшую неделю на двух языках. Аналогично создадим пост на тему «Депривация сна». 

![Новые посты на русском](image/newposts.png){ #fig:001 width=70% }

![Новые посты на английском](image.en/newposts.png){ #fig:001 width=70% }

21. Последний шаг для изменения репозитория:
```
git add .
git commit -am "sixth week"
git push
```

# Выводы

Сделала сайт двуязычным, перевела материалы на английский и русский и создала посты на двух языках. 
