---
## Front matter
title: "Отчёт по лабораторной работе №4


Математические основы защиты информации и информационной безопасности"
subtitle: "Вычисление наибольшего общего делителя"
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

Изучить алгоритмы нахождения наибольшего общего делителя и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация алгоритма Евклида

Алгоритм Евклида — эффективный алгоритм для нахождения наибольшего общего 
делителя двух целых чисел (или общей меры двух отрезков). Алгоритм назван в честь греческого математика Евклида 
(III век до н. э.), который впервые описал его в VII и X книгах «Начал».

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:001]) и (рис. [-@fig:002]):

![Реализация алгоритма Евклида](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация алгоритма Евклида](image/2.PNG){ #fig:002 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:003]):

![Проверка](image/3.PNG){ #fig:003 width=100% height=100% }

## Реализация бинарного алгоритма Евклида

Бинарный алгоритм Евклида — метод нахождения наибольшего общего делителя двух целых чисел. 
Данный алгоритм «быстрее» обычного алгоритма Евклида, так как вместо медленных операций деления и умножения используются сдвиги. 
Но это преимущество в скорости теряется с увеличением разницы между целыми числами более чем на несколько порядков, 
в результате чего число итераций вычитания может многократно превышать число итераций обычного алгоритма, использующего сравнение по модулю. 
То есть скорость бинарных сдвигов даёт эффект только для чисел, близких друг к другу.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:004]) и (рис. [-@fig:005]):

![Реализация бинарного алгоритма Евклида](image/4.PNG){ #fig:004 width=100% height=100% }

![Реализация бинарного алгоритма Евклида](image/5.PNG){ #fig:005 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:006]):

![Проверка](image/6.PNG){ #fig:006 width=100% height=100% }

## Реализация расширенного алгоритма Евклида

Расширенный алгоритм Евклида — модификация алгоритма Евклида, вычисляющая, 
кроме наибольшего общего делителя (НОД) целых чисел $a$ и $b$, ещё и коэффициенты соотношения Безу, 
то есть такие целые $x$ и $y$, что $ax + by =$ НОД(a , b).

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:007]) и (рис. [-@fig:008]):

![Реализация расширенного алгоритма Евклида](image/7.PNG){ #fig:007 width=100% height=100% }

![Реализация расширенного алгоритма Евклида](image/8.PNG){ #fig:008 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:009]):

![Проверка](image/9.PNG){ #fig:009 width=100% height=100% }

## Реализация расширенного бинарного алгоритма Евклида

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:010] - рис. [-@fig:012]):

![Реализация расширенного бинарного алгоритма Евклида](image/10.PNG){ #fig:010 width=100% height=100% }

![Реализация расширенного бинарного алгоритма Евклида](image/11.PNG){ #fig:011 width=100% height=100% }

![Реализация расширенного бинарного алгоритма Евклида](image/12.PNG){ #fig:012 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:013]):

![Проверка](image/13.PNG){ #fig:013 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/