---
## Front matter
title: "Отчёт по лабораторной работе №3


Математические основы защиты информации и информационной безопасности"
subtitle: "Шифрование гаммированием"
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

Изучить шифрование гаммированием и научиться его реализовывать.

# Выполнение лабораторной работы

## Реализация шифрования гаммированием

Шифрование гаммированием (или шифр XOR) — это метод симметричного 
шифрования, при котором открытый текст посимвольно «складывается» с гаммой 
(ключом), состоящей из случайной последовательности, используя операцию сложения по модулю. 
Этот процесс выполняется как при шифровании, так и при расшифровке, обеспечивая теоретически абсолютную стойкость, 
если длина гаммы не меньше длины сообщения.

Выполним реализацию этого шифрования на языке Julia (рис. [-@fig:001] - рис. [-@fig:004]):

![Реализация шифрования гаммированием](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация шифрования гаммированием](image/2.PNG){ #fig:002 width=100% height=100% }

![Реализация шифрования гаммированием](image/3.PNG){ #fig:003 width=100% height=100% }

![Реализация шифрования гаммированием](image/4.PNG){ #fig:004 width=100% height=100% }

Проверим работу шифрования гаммированием (рис. [-@fig:005]):

![Проверка](image/5.PNG){ #fig:005 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/