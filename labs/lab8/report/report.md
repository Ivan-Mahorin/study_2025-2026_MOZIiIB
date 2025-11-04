---
## Front matter
title: "Отчёт по лабораторной работе №8


Математические основы защиты информации и информационной безопасности"
subtitle: "Целочисленная арифметика многократной точности"
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

Изучить алгоритмы для выполнения арифметических операций с большими целыми числами и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация алгоритма 1 (сложение неотрицательных целых чисел)

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:001]) и (рис. [-@fig:002]):

![Реализация алгоритма 1](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация алгоритма 1](image/2.PNG){ #fig:002 width=100% height=100% }

## Реализация алгоритма 2 (вычитание неотрицательных целых чисел)

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:003]):

![Реализация алгоритма 2](image/3.PNG){ #fig:003 width=100% height=100% }

## Реализация алгоритма 3 (умножение неотрицательных целых чисел столбиком)

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:004]):

![Реализация алгоритма 3](image/4.PNG){ #fig:004 width=100% height=100% }

## Реализация алгоритма 5 (деление многоразрядных целых чисел)

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:005]):

![Реализация алгоритма 5](image/5.PNG){ #fig:005 width=100% height=100% }

Проверим работу алгоритмов (рис. [-@fig:006]):

![Проверка](image/6.PNG){ #fig:006 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/