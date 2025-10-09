---
## Front matter
title: "Отчёт по лабораторной работе №5


Математические основы защиты информации и информационной безопасности"
subtitle: "Вероятностные алгоритмы проверки чисел на простоту"
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

Изучить вероятностные алгоритмы проверки чисел на простоту и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация вычисления символа Якоби

Символ Якоби — теоретико-числовая функция двух аргументов, введённая К. Якоби в 1837 году. Является квадратичным характером 
в кольце вычетов. Символ Якоби обобщает символ Лежандра на все нечётные числа, большие единицы. Символ Кронекера — Якоби, 
в свою очередь, обобщает символ Якоби на все целые числа, но в практических задачах символ Якоби играет гораздо более важную роль, 
чем символ Кронекера — Якоби.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:001]) и (рис. [-@fig:002]):

![Реализация вычисления символа Якоби](image/1.PNG){ #fig:001 width=100% height=100% }

![Реализация вычисления символа Якоби](image/2.PNG){ #fig:002 width=100% height=100% }

## Реализация алгоритма, реализующего тест Ферма

Тест простоты Ферма в теории чисел — это тест простоты натурального числа $n$, основанный на малой теореме Ферма.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:003]):

![Реализация алгоритма, реализующего тест Ферма](image/3.PNG){ #fig:003 width=100% height=100% }

## Реализация алгоритма, реализующего тест Соловэя-Штрассена

Тест Соловея—Штрассена — вероятностный тест простоты, открытый в 1970-х годах Робертом Мартином Соловеем совместно с Фолькером Штрассеном. 
Тест всегда корректно определяет, что простое число является простым, но для составных чисел с некоторой вероятностью он может 
дать неверный ответ. Основное преимущество теста заключается в том, что он, в отличие от теста Ферма, распознает числа Кармайкла 
как составные.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:004]):

![Реализация алгоритма, реализующего тест Соловэя-Штрассена](image/4.PNG){ #fig:004 width=100% height=100% }

## Реализация алгоритма, реализующего тест Миллера-Рабина

Тест Миллера—Рабина — вероятностный полиномиальный тест простоты. Тест Миллера—Рабина, наряду с тестом Ферма и тестом 
Соловея—Штрассена, позволяет эффективно определить, является ли данное число составным. Однако, с его помощью нельзя 
строго доказать простоту числа. Тем не менее тест Миллера—Рабина часто используется в криптографии для получения больших 
случайных простых чисел.

Выполним реализацию этого алгоритма на языке Julia (рис. [-@fig:005]) и (рис. [-@fig:006]):

![Реализация алгоритма, реализующего тест Миллера-Рабина](image/5.PNG){ #fig:005 width=100% height=100% }

![Реализация алгоритма, реализующего тест Миллера-Рабина](image/6.PNG){ #fig:006 width=100% height=100% }

Проверим работу алгоритмов (рис. [-@fig:007]):

![Проверка](image/7.PNG){ #fig:007 width=100% height=100% }

# Список литературы. Библиография

[1] Julia: https://docs.julialang.org/en/v1/