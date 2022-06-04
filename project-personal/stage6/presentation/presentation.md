---
## Front matter
lang: ru-RU
title: Презентация ИП этап 6
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

# Презентация ИП этап 6

## Задание

* Сделать поддержку английского и русского языков.
* Разместить элементы сайта на обоих языках.
* Разместить контент на обоих языках.
* Сделать пост по прошедшей неделе.
* Добавить пост на тему по выбору (на двух языках). 

# Выполнение лабораторной работы

## Запускаю ~/bin/hugo server и начинаю работать с сайтом 

##  Захожу в файл macblog/config/_default/languages.yaml. Добавляю туда русский язык

![macblog/config/_default/languages.yaml](image/lang.png){ #fig:001 width=70% }

## Меняю файл menus.yaml на файлы menus.ru.yaml и menus.en.yaml

![Файлы](image/menuses.png){ #fig:001 width=70% }

![menus.ru.yaml](image/menus.ru.png){ #fig:001 width=70% }

## Далее идем в папку content и создаем там две папки ru и en

![content](image/content.png){ #fig:001 width=70% }

## Начинаем переводить данные на русский. Достижения:

![Достижения](image/accom1.png){ #fig:001 width=70% }

![Достижения](image/accom2.png){ #fig:001 width=70% }

## Контакты:

![Контакты](image/contact1.png){ #fig:001 width=70% }

![Контакты](image/contact2.png){ #fig:001 width=70% }

## События:

![События](image/event1.png){ #fig:001 width=70% }

![События](image/event2.png){ #fig:001 width=70% }

## Опыт:

![Опыт](image/exper1.png){ #fig:001 width=70% }

![Опыт](image/exper2.png){ #fig:001 width=70% }

## Избранные публикации:

![Избранные публикации](image/featured1.png){ #fig:001 width=70% }

![Избранные публикации](image/featured2.png){ #fig:001 width=70% }

## Посты:

![Посты](image/post1.png){ #fig:001 width=70% }

![Посты](image/post2.png){ #fig:001 width=70% }

## Проекты:

![Проекты](image/proj1.png){ #fig:001 width=70% }

![Проекты](image/proj2.png){ #fig:001 width=70% }

## Публикации:

![Публикации](image/publish1.png){ #fig:001 width=70% }

![Публикации](image/publish2.png){ #fig:001 width=70% }

## Навыки:

![Навыки](image/skills1.png){ #fig:001 width=70% }

![Навыки](image/skills2.png){ #fig:001 width=70% }

## Теперь переведем некоторые разделы на английский. Биография:

![Биография](image.en/bio.png){ #fig:001 width=70% }

## Контакты:

![Контакты](image.en/contact.png){ #fig:001 width=70% }

## Публикации:

![Публикации](image.en/public.png){ #fig:001 width=70% }

## Достижения и посты:

![Достижения и посты](image.en/accomppost.png){ #fig:001 width=70% }

## Проекты и события:

![Проекты и события](image.en/projevent.png){ #fig:001 width=70% }

## Навыки и опыт: 

![Навыки и опыт](image.en/skillandexp.png){ #fig:001 width=70% }

## Далее создадим пост про прошедшую неделю на двух языках. Аналогично создадим пост на тему «Депривация сна». 

![Новые посты на русском](image/newposts.png){ #fig:001 width=70% }

![Новые посты на английском](image.en/newposts.png){ #fig:001 width=70% }

## Последний шаг для изменения репозитория:
```
git add .
git commit -am "sixth week"
git push
```

# Выводы

Сделала сайт двуязычным, перевела материалы на английский и русский и создала посты на двух языках
