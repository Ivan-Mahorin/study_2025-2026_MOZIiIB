---
## Front matter
lang: ru-RU
title: Лабораторная работа №1
subtitle: Математические основы защиты информации и информационной безопасности
author:
  - Махорин И. С.
institute:
  - Российский университет дружбы народов имени Патриса Лумумбы, Москва, Россия
date: 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Махорин Иван Сергеевич
  * Студент группы НФИмд-02-25
  * Студ. билет 1032259380
  * Российский университет дружбы народов имени Патриса Лумумбы

:::
::: {.column width="30%"}

![](./image/0.jpg)

:::
::::::::::::::


## Цель лабораторной работы

- Изучить шифры простой замены и научиться их реализовывать.

# Выполнение лабораторной работы

## Реализация шифра Цезаря с произвольным ключом K

![Реализация шифра цезаря с произвольным ключом K](image/1.PNG){ #fig:001 width=70% height=70% }

##  Проверка

![Проверка](image/2.PNG){ #fig:002 width=70% height=70% }

##  Реализация шифра Атбаш

![Реализация шифра Атбаш](image/3.PNG){ #fig:003 width=70% height=70% }

## Проверка

![Проверка](image/4.PNG){ #fig:004 width=70% height=70% }

# Вывод

## Вывод

- В ходе выполнения лабораторной работы были изучены шифры простой замены, а также
написаны их алгоритмы на языке Julia.

# Список литературы. Библиография

[[1] Julia: https://docs.julialang.org/en/v1/