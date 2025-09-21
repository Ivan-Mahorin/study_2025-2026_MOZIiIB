---
## Front matter
title: "Отчёт по лабораторной работе №1


Математические основы защиты информации и информационной безопасности"
subtitle: "Шифры простой замены"
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

Изучить шифры простой замены и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация шифра Цезаря с произвольным ключом K

Шифр Цезаря — это древнейший шифр подстановки, в котором каждая буква исходного 
текста заменяется другой буквой, сдвинутой на фиксированное число позиций в алфавите. 
Этот метод очень прост: например, при сдвиге на 3, А становится Г, Б — Д и так далее. 
Для восстановления исходного текста нужно сдвинуть буквы в обратном направлении.  

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:001]):

![Реализация шифра цезаря с произвольным ключом K](image/1.PNG){ #fig:001 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:002]):

![Проверка](image/2.PNG){ #fig:002 width=100% height=100% }

## Реализация шифра Атбаш

Шифр Атбаш — это простейший шифр замены, в котором буквы алфавита заменяются в обратном порядке: первая буква становится последней, 
вторая — предпоследней и так далее. Например, A становится Z, B — Y, а C — X. Этот метод изначально применялся для еврейского алфавита, 
откуда и получил свое название от первых букв «алеф» и «тав»:

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:003]):

![Реализация шифра Атбаш](image/3.PNG){ #fig:003 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:004]):

![Проверка](image/4.PNG){ #fig:004 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/