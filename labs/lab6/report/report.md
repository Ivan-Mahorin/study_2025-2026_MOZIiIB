---
## Front matter
title: "Отчёт по лабораторной работе №6


Математические основы защиты информации и информационной безопасности"
subtitle: "Разложение чисел на множители"
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

Изучить алгоритм разложения чисел на множители и научиться его реализовывать.

# Выполнение лабораторной работы

## Реализация вычисления символа Якоби

Ро-алгоритм — предложенный Джоном Поллардом в 1975 году алгоритм, служащий для факторизации (разложения на множители) целых чисел. 
Данный алгоритм основывается на алгоритме Флойда поиска длины цикла в последовательности и некоторых следствиях из парадокса дней рождения. 
Алгоритм наиболее эффективен при факторизации составных чисел с достаточно малыми множителями в разложении.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:001] - рис. [-@fig:006]):

![Реализация р-Метода Полларда](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация р-Метода Полларда](image/2.PNG){ #fig:002 width=100% height=100% }

![Реализация р-Метода Полларда](image/3.PNG){ #fig:003 width=100% height=100% }

![Реализация р-Метода Полларда](image/4.PNG){ #fig:004 width=100% height=100% }

![Реализация р-Метода Полларда](image/5.PNG){ #fig:005 width=100% height=100% }

![Реализация р-Метода Полларда](image/6.PNG){ #fig:006 width=100% height=100% }

Проверим работу алгоритма (рис. [-@fig:007]):

![Проверка](image/7.PNG){ #fig:007 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/