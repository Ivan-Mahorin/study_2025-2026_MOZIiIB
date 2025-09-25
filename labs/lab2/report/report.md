---
## Front matter
title: "Отчёт по лабораторной работе №2


Математические основы защиты информации и информационной безопасности"
subtitle: "Шифры перестановки"
author: "Выполнил: Махорин Иван Сергеевич, 


НФИмд-02-21, 1032259380"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: _resources/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить шифры перестановки и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация маршрутного шифрования

Данный способ шифрования разработал французский математик Франсуа
Виет. Открытый текст записывают в некоторую геометрическую фигуру (обычно
прямоугольник) по некоторому пути, а затем, выписывая символы по другому
пути, получают шифртекст.

Выполним реализацию этого шифрования на языке Julia (рис. [-@fig:001]) и (рис. [-@fig:002]):

![Реализация маршрутного шифрования](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация маршрутного шифрования](image/2.PNG){ #fig:002 width=100% height=100% }

Проверим работу маршрутного шифрования (рис. [-@fig:003]):

![Проверка](image/3.PNG){ #fig:003 width=100% height=100% }

## Реализация шифрования с помощью решеток

Данный способ шифрования предложил австрийский криптограф Эдуард
Флейснер в 1881 году. Суть этого способа заключается в следующем. Выбирается
натуральное число $k > 1$, строится квадрат размерности $k$ и построчно
заполняется числами $1, 2, ..., k^2$.

Выполним реализацию этого шифрования на языке Julia (рис. [-@fig:004] - рис. [-@fig:006]):

![Реализация шифрования с помощью решеток](image/4.PNG){ #fig:004 width=100% height=100% }

![Реализация шифрования с помощью решеток](image/5.PNG){ #fig:005 width=100% height=100% }

![Реализация шифрования с помощью решеток](image/6.PNG){ #fig:006 width=100% height=100% }

Проверим работу шифрования с помощью решеток (рис. [-@fig:007]):

![Проверка](image/7.PNG){ #fig:007 width=100% height=100% }

## Реализация таблицы Виженера

В 1585 году французский криптограф Блез Виженер опубликовал свой метод
шифрования в «Трактате о шифрах». Шифр считался нераскрываемым до 1863
года, когда австриец Фридрих Казиски взломал его.

Выполним реализацию этого шифрования на языке Julia (рис. [-@fig:008]) и (рис. [-@fig:009]):

![Реализация таблицы Виженера](image/8.PNG){ #fig:008 width=100% height=100% }

![Реализация таблицы Виженера](image/9.PNG){ #fig:009 width=100% height=100% }

Проверим работу таблицы Виженера (рис. [-@fig:010]):

![Проверка](image/10.PNG){ #fig:010 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/